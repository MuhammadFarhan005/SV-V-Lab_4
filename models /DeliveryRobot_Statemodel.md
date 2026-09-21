# Autonomous Delivery Robot — State Model

| State_ID | State_name | Description | Entry Condition | Exit Condition |
|---|---|---|---|---|
| S1 | IDLE | Robot is waiting for a delivery request. | Robot is switched on or reaches the warehouse. | Delivery request is received. |
| S2 | NAVIGATING | Robot is moving toward the delivery destination. | A delivery request is received. | Destination is reached, obstacle is detected, or battery becomes critically low. |
| S3 | AVOIDING_OBSTACLE | Robot temporarily stops normal navigation and handles an obstacle. | An obstacle is detected while navigating. | Obstacle is successfully avoided. |
| S4 | DELIVERING | Robot is performing the package delivery at the destination. | Robot reaches the destination. | Package is successfully delivered. |
| S5 | RETURNING | Robot is traveling back toward the warehouse. | Delivery is successful or battery becomes critically low during navigation. | Warehouse is reached. |
