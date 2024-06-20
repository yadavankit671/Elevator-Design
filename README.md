# Elevator Design in Java #
This project simulates a basic elevator system using Java. It handles requests from both inside and outside the elevator, prioritizing requests based on the elevator's current direction and the requested floors.
# Elevator Design in Java #
This project simulates a basic elevator system using Java. It handles requests from both inside and outside the elevator, prioritizing requests based on the elevator's current direction and the requested floors.

## Features ##
- <b>Request Handling: </b> Accepts requests with details like current floor, desired floor, direction (UP/DOWN), and location (INSIDE/OUTSIDE).
- <b>Prioritized Queues: </b>Uses priority queues to manage and prioritize requests based on the direction of travel.
- <b>Efficient Operation: </b>Optimizes elevator movement by grouping requests in the same direction together.
- <b>Inside/Outside Handling: </b>Differentiates between requests from inside and outside the elevator, ensuring pickup from the current floor if requested from outside.
<br>
## Classes ##
* `Request`: Represents a single elevator request with details about the requester's current floor, desired floor, direction, and location.
* `Elevator`: 
    - Maintains the elevator's state(current floor, direction). 
    - Handles `sendUpRequest` and `sendDownRequest` methods to add requests to respective priority queues. 
    - Implements the `run` method to process all queued requests efficiently.
* `App`: Provides a basic simulation of the elevator system with sample requests.

## How to Run
**Compilation**: <br> To compile the source file, use the following command: 
```
> javac App.java
```
**Execution**:<br>Run the compiled App class to start the program.

```
> java App
```

## How It Works ##
1. **Initialization**: The elevator starts at a specified floor and is initially IDLE.
2. **Request Submission**: Requests are created and submitted to the elevator using `sendUpRequest` and `sendDownRequest`.
3. **Prioritization**: Requests are added to priority queues (`upQueue` and `downQueue`) based on their direction and desired floor.
4. **Processing**: The `run` method iterates through the queues:
    - If the elevator is going UP or IDLE, it processes UP requests first, then DOWN requests.
    - If the elevator is going DOWN, it processes DOWN requests first, then UP requests.
5. **Movement Simulation**: The elevator's current floor is updated to the desired floor of each processed request, simulating movement.

### Notes
> This implementation is kept simplified. We can customize and integrate more complex logic, handling multiple elevators, door operations and error conditions.

