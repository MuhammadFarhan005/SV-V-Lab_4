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
