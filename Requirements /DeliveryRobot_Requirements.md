# Autonomous Delivery Robot — Requirements

| Req_ID | Description | Priority |
|---|---|---|
| R1 | The robot shall remain in the IDLE state after being switched on until a delivery request is received. | High |
| R2 | The robot shall start navigating toward the requested destination when a delivery request is received. | High |
| R3 | The robot shall detect obstacles while it is navigating toward the destination. | High |
| R4 | When an obstacle is detected during navigation, the robot shall enter the AVOIDING_OBSTACLE state. | High |
| R5 | After successfully avoiding an obstacle, the robot shall resume navigation toward the destination. | High |
| R6 | When the robot reaches the destination, it shall start the delivery process. | High |
| R7 | The robot shall complete the delivery only after the package has been successfully delivered. | High |
| R8 | After successful delivery, the robot shall return to the warehouse. | High |
| R9 | If the battery becomes critically low during navigation, the robot shall stop the current journey and return to the warehouse. | High |
| R10 | When the robot reaches the warehouse, it shall enter the IDLE state and wait for another delivery request. | High |
