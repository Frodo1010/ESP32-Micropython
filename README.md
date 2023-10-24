# ESP32-Micropython
Hardware modules written in Micropython for the ESP32.

**Note**: Stepper motor outputs can vary. Some motors may have the configuration: 
- Coil1_IN, Coil1_MIDDLE, Coil1_END, 
- Coil2_IN, Coil2_MIDDLE, Coil2_END.

While others might follow: 
- Coil1_IN, Coil2_IN, 
- Coil1_MIDDLE, Coil2_MIDDLE, 
- Coil1_END, Coil2_END.


## Stepper_A4988
A module to control a bipolar stepper motor using an A4988 driver board.

### Functions:
- `move_step(speed)`: Moves the motor by one step.
- `move_inc(steps, speed=0.005)`: Moves the motor a specified number of steps relative to its current position.
- `move_abs(pos, speed=0.005)`: Moves the motor to an absolute position.
- `trigger_dir()`: Toggles the motor's direction.
- `trigger_zero()`: Resets the motor's position data to zero.
- `set_pos(pos)`: Sets the motor's current position.
- `get_position()`: Returns the current position data of the motor.
- `set_max_steps(number)`: Sets the maximum step count for micro-stepping and configures the driver accordingly.

