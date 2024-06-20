# Elevator Design in Java #
This project simulates a basic elevator system using Java. It handles requests from both inside and outside the elevator, prioritizing requests based on the elevator's current direction and the requested floors.

## Features ##
- <b>Request Handling: </b> Accepts requests with details like current floor, desired floor, direction (UP/DOWN), and location (INSIDE/OUTSIDE).
- <b>Prioritized Queues: </b>Uses priority queues to manage and prioritize requests based on the direction of travel.
- <b>Efficient Operation: </b>Optimizes elevator movement by grouping requests in the same direction together.
- <b>Inside/Outside Handling: </b>Differentiates between requests from inside and outside the elevator, ensuring pickup from the current floor if requested from outside.

  ## Classes
* `Request`: Represents a single elevator request with details about the requester's current floor, desired floor, direction, and location.
* `Elevator`: - 1.Maintains the elevator's state(current floor, direction). - 2. Handles `sendUpRequest` and `sendDownRequest` methods to add requests to respective priority queues. - 3. Implements the `run` method to process all queued requests efficiently.
* `App`: Provides a basic simulation of the elevator system with sample requests.
