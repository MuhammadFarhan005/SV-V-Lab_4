# Autonomous Delivery Robot — State Transition Table

| Transition_ID | From State | Event | To State | Requirement_ID |
|---|---|---|---|---|
| T1 | IDLE | Delivery Request Received | NAVIGATING | R1, R2 |
| T2 | NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE | R3, R4 |
| T3 | AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING | R5 |
| T4 | NAVIGATING | Destination Reached | DELIVERING | R6 |
| T5 | DELIVERING | Delivery Successful | RETURNING | R7, R8 |
| T6 | NAVIGATING | Critical Battery | RETURNING | R9 |
| T7 | RETURNING | Warehouse Reached | IDLE | R10 |

## Verification Checks

### Check 1 — Invalid Transition
IDLE → DELIVERING is invalid.

The robot must first receive a delivery request and navigate to the destination.
This violates R1, R2, and R6.

### Check 2 — Missing Transition
If AVOIDING_OBSTACLE does not transition back to NAVIGATING after the obstacle is avoided,
the robot cannot continue its delivery journey.

This violates R5.

### Check 3 — Obstacle During Delivery
There is no valid transition from AVOIDING_OBSTACLE directly to DELIVERING.

The robot must first return to NAVIGATING and then reach the destination before entering
the DELIVERING state.
