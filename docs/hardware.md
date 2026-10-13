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

## Buying it all from one place (Germany: Amazon.de)

Checked directly: Amazon.de is the one retailer that actually stocks every
category below — dev board, IMU, motor, driver board, testbed bearing,
logic analyzer, multimeter, breadboard kit, and buck converter. German
specialist shops don't cover the full list: Reichelt/Mouser/Digikey carry
the electronics (board, driver ICs, breadboards) but not RC motors or
lazy-susan bearings; BerryBase carries the IMU but not the motor or
bearing either. Amazon.de is the only single checkout that covers
everything.

| Item | Example Amazon.de listing found | Approx. price |
| --- | --- | --- |
| MCU dev board | [STM32 Nucleo-F411RE](https://www.amazon.de/-/en/NUCLEO-F411RE-Nucleo-64-Development-STM32F411RE-Connectivity/dp/B07JYF8RRB) | ~€38–43 |
| 9-DoF IMU breakout | [SparkFun ICM-20948 breakout](https://www.amazon.de/-/en/SparkFun-9DoF-IMU-Breakout-ICM-20948/dp/B07WGGDX8X) or [Pimoroni ICM20948 breakout](https://www.amazon.de/Pimoroni-ICM20948-Motion-Sensor-Breakout/dp/B07RLK17ZV) | ~€20–30 |
| Small BLDC motor | search "2208 gimbal brushless motor" — several listings, e.g. [FEICHAO 2208](https://www.amazon.de/FEICHAO-B%C3%BCrstenloser-Geschwei%C3%9Ft-Aircraft-Multicopter/dp/B08R1LL6TK) | ~€12–20 |
| 3-phase motor driver (ready-made) | [DRV8313-based "SimpleFOC Mini" driver board](https://www.amazon.de/CASNO-einfache-Mini-Motor-Treiberplatine-Steueralgorithmus-FOC-Steuerungstreiber/dp/B0D56R2GP7) — no soldering needed, better than the DIY option below | ~€6–13 |
| Low-friction 1-axis platform | lazy-susan ball-bearing turntable, search "Drehtellerlager Kugellager" | ~€20–40 (German Amazon pricing runs higher than US/UK for this item) |
| USB logic analyzer | [24MHz/8-channel clone](https://www.amazon.de/APKLVSR-Analyzer-USB-Kabel-8-Kanal-kompatibel/dp/B0CFFGS5XF) | ~€8–12 |
| Digital multimeter | [Hanmatek basic DMM](https://www.amazon.de/Digitalmultimeter-HANMATEK-Messbereichserkennung-NCV-Widerstand-Spannungserkennung/dp/B07JLXVPT4) or similar | ~€9–17 |
| Breadboard + jumper wire kit | search "Breadboard Jumper Kabel Set" | ~€7–15 |
| Adjustable DC-DC buck converter | [MP1584EN module, pack of several](https://www.amazon.de/MP1584-MP1584EN-verstellbarer-Abw%C3%A4rtswandler-Spannungsmodul/dp/B0CSTC97KQ) | ~€6–10 (for a pack — unit cost is a euro or two) |

**Estimated total via Amazon.de alone: roughly €170–200** for the core
parts above, plus a wall power adapter and misc small parts
(~€20–30 more, also on Amazon.de). That's noticeably more than ordering
from multiple specialist sources (below) — mainly because the Nucleo
board and the bearing turntable both run 2–3× pricier on Amazon.de than
their cheapest source elsewhere.

**One split worth making even if you want "mostly one place":** order the
Nucleo board from [Mouser.de](https://www.mouser.de) or
[Digikey.de](https://www.digikey.de) instead (~€14–18 there vs. ~€40 on
Amazon.de) — both ship to Germany, and that single swap saves ~€20–25 on
its own. Everything else can stay on Amazon.de in one cart.

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
