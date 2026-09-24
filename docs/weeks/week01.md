# Week 01 – Mathematical Foundations & Attitude Representations

**Month:** 1 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
An AOCS lead requires your own, testable attitude library, because in a flight-software context off-the-shelf packages can't be adopted without independent verification – external libraries are for cross-validation only.

## Task
a) Implement DCM↔quaternion and Euler(3-2-1)↔DCM conversions, each as pure functions.

b) Implement quaternion multiplication (document the convention explicitly, M&C 2.7) and the conjugate/inverse.

c) Implement the error quaternion δq = q⊗q_ref⁻¹ (M&C 2.10) including the small-angle approximation δq≈[δα/2;1].

d) Property tests with ≥1000 random rotations: round-trip DCM→quat→DCM to < 1e-9 Frobenius distance, ‖q‖=1 after every operation.

e) Demonstrate gimbal lock numerically: construct a 3-2-1 sequence near θ=90° pitch, show the rank loss of the Jacobian, and compare with the quaternion representation of the same rotation.

f) Cross-validate the same 1000 rotations against `scipy.spatial.transform.Rotation` (deviation < 1e-9); scipy remains a verification tool only, not a project dependency.

## Acceptance Criteria
all tests green, test coverage of `attitude/` ≥ 95%, gimbal-lock demonstration with numbers in the devlog.

## Deliverable
`attitude/` module + `tests/test_attitude.py`, devlog with gimbal-lock analysis.

## My Notes
_(to be filled in by me during the week)_
