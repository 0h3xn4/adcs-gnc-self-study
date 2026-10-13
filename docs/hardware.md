# Hardware Bill of Materials (Budget Build)

This expands Section 3.2 of the curriculum (hardware for Week 0's ordering
task) into concrete, cheap parts. It's for the physical testbed used from
Month 2 onward (Weeks 5–17, 23–24) — Months 1 and 5 are pure software and
need no hardware at all.

**Prices are approximate** (checked October 2026), vary by region/
shipping/import duties, and AliExpress-type clone prices in particular
fluctuate — treat every number here as "roughly this much," not a quote,
and check current listings before ordering. Where a specific clone/
AliExpress price isn't verifiable, that's noted instead of guessed.

## Buying it in Germany, no Amazon, no eBay

Checked directly, deliberately excluding both marketplaces: **no single
traditional German retailer stocks everything on this list** — the mix of
professional dev board, maker-electronics IMU, RC-hobby motor, and a
household-style bearing straddles categories that German retail splits
across different specialist shops. The closest to one-stop, with real
listings confirmed, is **three retailers, zero marketplaces**:

A note on the stock column below: I don't have live access to these
retailers' sites (direct page fetches to conrad.de/reichelt.de/
berrybase.de are blocked from this environment), so "stock" here comes
from search-engine snapshots of their pages, which are sometimes
contradictory between pages for the same product and can lag the live
site. Treat it as "recently seen as available," not a real-time
guarantee — confirm in the shop's own cart before relying on it.

| Item | Retailer | Specific listing found | Stock signal seen | Approx. price |
| --- | --- | --- | --- | --- |
| MCU dev board | [Conrad.de](https://www.conrad.de) | STMicroelectronics NUCLEO-F411RE | 28 units, same-day dispatch | ~€17.64 (+VAT) |
| Digital multimeter | Conrad.de | VOLTCRAFT VC131 | consistently 2,500+ units across multiple pages — very safe bet | ~€17–22 |
| Breadboard + jumper wire kit | Conrad.de | Joy-it Breadboard 830 | 698 units | ~€10–15 |
| Low-friction 1-axis platform | Conrad.de | axial ball bearing, e.g. FAG 51101 (26mm) or FAG 51105 (42mm) | 17–108 units depending on size, several sizes in stock | ~€5–15 |
| Small BLDC motor | Conrad.de | Pichler "Boost 18" (1050 kV, 35mm×28mm, 75g) — closest in-stock match; a specific 2208 motor I checked was explicitly **not available** and a Reely 960kV motor was **sold out**, so verify the exact model before ordering | only 4 units seen — **tightest item on this list, check first** | ~€15–25 |
| 9-DoF IMU breakout | [BerryBase.de](https://www.berrybase.de) | **Adafruit** ICM-20948 (STEMMA QT) — more consistently shown available than the SparkFun version, which had one listing marked "currently not available" | 34 units on the category page, 4 on a product page — consistently positive signal | ~€20 |
| USB logic analyzer | BerryBase.de | SparkFun USB Logic Analyzer, 24MHz/8-channel | **Conflicting signals** — one page showed 7 in stock, another (and the French-locale page) showed "no longer available" — this is the least certain item here | ~€30 |
| 3-phase motor driver | [Reichelt.de](https://www.reichelt.de) | bare **L6234** driver IC (SOP-20, 7–52 V, 5 A), [product page](https://www.reichelt.de/motortreiber-3-fach-sop-20-l-6234-pd-p109314.html) + a small perfboard breakout you solder yourself | not confirmed in this pass — check the product page directly | IC ~€4–6 + perfboard/headers ~€5 = **~€10** |
| Adjustable DC-DC buck converter | Reichelt.de or Conrad.de | general step-down module | not confirmed — neither retailer's listing for an MP1584-specific adjustable module showed up in search | ~€5–10 |

**Estimated total: roughly €110–150** for the core parts above, plus a
wall power adapter and misc small parts (~€20–30 more, also from
Conrad.de). Three checkouts instead of one, plus the caveats above:

- **The motor** is the weakest-confirmed item: the specific small,
  cheap options are low-stock or already out at Conrad. Check "Flugmodell
  Brushless-Elektromotoren" for whatever's currently in stock in the
  ~30–80g range rather than committing to one exact model from this
  table.
- **The logic analyzer** at BerryBase had genuinely conflicting
  availability signals between pages — worth double-checking directly,
  or falling back to Reichelt's general test-equipment section if it's
  actually out.
- **The motor driver** stays the DIY bare-IC-plus-perfboard route, since
  no German retailer (marketplace or not) turned up a ready-made DRV8313/
  SimpleFOC-style board — Pololu sells a ready brushless controller
  through exp-tech.de, but it does its own FOC internally, which defeats
  the point of Week 15's "implement your own commutation" task.

## Core parts (cheapest overall, ordering from multiple sources)

Prices below are from the original international research (USD, mostly
US distributors) — Mouser.de, Digikey.de, and RS Components Germany serve
the same parts to Germany at roughly the same EUR magnitude, so treat
"$" here as "≈€" rather than converting.

| Item | Used from | Cheapest verified option | Approx. price | Cheaper alternative |
| --- | --- | --- | --- | --- |
| MCU dev board | Week 6 onward | [STM32 Nucleo-F411RE](https://www.digikey.com/en/products/detail/stmicroelectronics/NUCLEO-F411RE/4866485) — good HAL docs, on-board ST-Link debugger, no extra programmer needed | ~$13–18 (Arrow/Digi-Key/Mouser) | None cheaper with comparable documentation quality — this is the one place not to cut corners, since Week 6–8 debugging depends on usable docs |
| 9-DoF IMU breakout | Week 6 onward | [Adafruit ICM-20948 (STEMMA QT)](https://www.adafruit.com/product/4554) | ~$20 | Generic ICM-20948/MPU-9250 clone boards exist on AliExpress for ~$5–8, but quality/documentation is unverified — fine if you're comfortable debugging a flaky breakout, riskier for Week 6's first bring-up |
| Small BLDC motor (reaction-wheel analog) | Week 7 onward | Sensorless 2208/2204 gimbal motor (e.g. Lumenier GX2208-80 class) | ~$10–18 | Skip the Hall-sensor version (~$20–40, e.g. JD-Power DCH-3518C) unless you specifically want Hall-based speed sensing in Week 7 instead of BEMF zero-crossing — the curriculum's Task explicitly allows either |
| 3-phase motor driver | Week 15 onward | Bare **L6234** or **DRV8313** driver IC (~$3–4 each, e.g. [RS Components](https://ph.rs-online.com/web/p/motor-driver-ics/1961930)) + a small perfboard breakout you solder yourself | IC ~$4 + perfboard/headers ~$5 = **~$9** | A pre-made breakout (old SparkFun/MikroE "Brushless Click") runs ~$20–30 when available — worth it only if SMD soldering (HTSSOP/PowerSO package) is a hard blocker for you |
| Low-friction 1-axis platform | Week 16 onward | 4″ lazy-susan ball-bearing turntable ([Busy Bee](https://www.busybeetools.com/products/lazy-susan-4in), ~$9; or [Simply Bearings](https://www.simplybearings.co.uk/products/lazy-4), ~£4.50 ex VAT) | ~$9 | **Free–$3:** a bifilar fishing-line suspension (two lines from a fixed point to the testbed) — the curriculum explicitly calls this out as a valid low-cost alternative to an air-bearing table |
| USB logic analyzer | Week 7, 15 | Generic 24 MHz/8-channel Saleae-style clone | ~$10 (range seen: $6–20 depending on seller/region) | None cheaper that still works with free software — get the clone, then install [sigrok/PulseView](https://sigrok.org/) (free, open source) **before** it arrives so you can confirm it's recognized |
| Digital multimeter | Week 6 onward | Any basic DMM (continuity, DC voltage/current, resistance) | ~$10–15 | Sub-$7 meters exist (hardware-store own-brand) and are fine for this project's low-voltage DC work — just never use a cheap meter on mains/AC power |

## Supporting basics (not itemized in the curriculum, but needed)

| Item | Why | Approx. price |
| --- | --- | --- |
| Breadboard + jumper wire kit | Prototyping before anything is soldered | ~$10 |
| Adjustable DC-DC buck converter module (e.g. MP1584-based) | Regulates a wall adapter down to the motor driver's/MCU's supply voltage | ~$3–5 |
| 12 V DC wall power adapter (~2 A) | Bench power for the motor driver — safer and cheaper than a LiPo + charger for this project | ~$10 |
| Resistor/capacitor assortment kit | Pull-ups, decoupling, gate resistors, etc. | ~$6–8 |
| Misc: standoffs/screws, double-sided tape, zip ties, a few USB cables | Mounting the testbed, cable management | ~$10 |

## Optional / stretch

| Item | For | Approx. price | Note |
| --- | --- | --- | --- |
| Helmholtz coil pair | Month 4 buffer week magnetorquer experiment | ~$10–15 in magnet wire + a cardboard/PVC tube (DIY wind, no kit needed) | Purely a stretch goal — skip it entirely if money's tight; nothing else in the curriculum depends on it |

## Estimated total

**Core parts + supporting basics: roughly $100–140.** The two items worth
not cutting (MCU board, IMU) are also the two with the best documentation
— a $5 clone IMU that doesn't match its datasheet costs you more time in
Week 6 debugging than the $15 you saved. Everything else (motor, driver,
testbed platform, logic analyzer) has a genuinely free-to-cheap path if
needed:

- Fishing-line suspension instead of a bearing turntable: **saves ~$9**
- Sensorless motor instead of Hall-sensor: **saves ~$10–25**
- DIY MOSFET half-bridges instead of a driver IC (3× generic N-channel
  MOSFET, e.g. IRLZ44N, ~$1 each) if you want to build the power stage
  from scratch too: **saves ~$6**, at the cost of more wiring and a less
  forgiving driver — only recommended if you're already comfortable with
  gate drive circuits.

With every cut taken, a working testbed is achievable for well under
$100 — just budget extra debugging time against the clone IMU and the
from-scratch driver.
