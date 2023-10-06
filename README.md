
# Rocket Opportunity's **Board Computer**
## Introduction
Welcome to Rocket Opportunity's Board Computer v2.3.2! This project, written in C++ using Arduino modules and libraries, is a culmination of months of dedicated effort to design, develop, and test a functional model rocket board computer. This computer is responsible for monitoring the rocket's flight, making real-time calculations, deploying the parachute, and logging sensor data.

Check out this poster showcasing an early iteration of the computer and rocket <a href="https://drive.google.com/file/d/1Fb76lBiJfNJNnFR3AuLNGKqBDm8GRUav/view?usp=sharing">here</a>.

## Development Phases
The project unfolded in three phases:
1. <b>Physical Board Design (Phase 1):</b> This involved designing and building the physical computer, incorporating sensors, servo motors, and an Arduino Nano board running at 16 MHz with an ATmega328P processor.<br><br>
2. **Flight Algorithm Development (Phase 2):** The flight algorithm, written in C++, was designed and developed to ensure optimal performance during different flight states.<br><br>
3. **Testing (Phase 3):** The board underwent rigorous testing, both in terms of its physical components and software functionality. Various iterations were flown, outcomes were analyzed, and new generations of the board were developed.

## Flight States
The board operates in different states, each tuned to specific sensors and calculations:

- GROUND_IDLE: Board is idle on the ground, awaiting launch.
- POWERED_FLIGHT: Rocket is powered and ascending.
- UNPOWERED_FLIGHT: Rocket is coasting without power.
- BALISTIC_DESCENT: Rocket is descending without parachute.
- PARACHUTE_DEPLOYMENT: Parachute is deployed.
- PARACHUTE_DESCENT: Rocket descends safely with the parachute.
- LANDING_SAFE: Rocket safely lands.

Here, you can find a graphical representation of the flight stages: <a href="https://drive.google.com/file/d/1HfgYe8Wp4lQ2HgKxz4R57NoND0g4JFa2/view?usp=drive_link">FlightStages.pdf</a>.


## Instruction of Use
1. Booting Up:
      - LED on
      - 3-tone buzz from the speaker

2. Waiting for Command:
      - LED off
      - No sound

3. Armed and Running:
      - Press button for arming the PC
      - Alarm sound buzzer
      - Small flash + bip sound every 2 seconds
      
4. Any Error:
      - Every process will stop
      - The BC will flash the LED

## Contents
- Arduino Nano Board:

     - The brain of the computer, running at 16 MHz.
     - Can perform tens of millions of instructions per second.
     - ATmega328P executes 1 instruction per clock cycle.

- Accelerometer:

     - Measures g-forces and indicates the rocket's orientation.
     - Assists in calculating different thresholds to cycle through flight states.

- Barometer:

     - Registers air pressure to calculate altitude during flight.

- SD Card Module:

     - Logs all flight data as well as sensor data for analysis.

- SERVO Motors:

     - The way the computer interacts with the physical world.
     - Used for tasks like deploying the parachute.
