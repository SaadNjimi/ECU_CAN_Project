# ECU_CAN_Project

## Overview

This project demonstrates the development of an Electronic Control Unit (ECU) application with CAN bus communication, created as part of a university course in automotive software engineering. The ECU interacts with a virtual dashboard simulator (**VirtualCockpit**) by sending and receiving CAN messages to control vehicle indicators such as speed, RPM, and lights.

---

## Features

- Configured CAN controller for message transmission and reception (standard & extended frames).
- Implemented message filtering for CAN IDs 0x10 and 0x11.
- Interrupt-driven CAN message handling with LED indicators.
- Periodic CAN messages to control virtual dashboard elements:
  - Vehicle speed mapped from analog potentiometer input (0–240 km/h).
  - Cyclic RPM pattern generation.
  - Indicator and light control based on input switches.
- Integration with VirtualCockpit for real-time ECU simulation and validation.

---

## Technologies & Tools

- **Programming Language:** C (Embedded)
- **Hardware:** Microcontroller with CAN Bus support
- **Software Tools:** VirtualCockpit (dashboard simulator), CAN protocol stack

---

## Project Structure

- `source/siu.c` — CAN controller pin configuration and initialization  
- `source/can.c` — CAN message buffer setup and transmission functions  
- `main.c` — Main program logic, message handling, and LED control  
- Additional headers and configs for CAN filtering and buffer management  

---

## Usage Instructions

1. Set up the microcontroller hardware and connect it to the CAN bus.  
2. Launch the VirtualCockpit tool on your development PC.  
3. Compile and flash the ECU firmware to the microcontroller.  
4. Use VirtualCockpit to send “Start Engine” (ID 0x11) and “Stop Engine” (ID 0x10) CAN messages.  
5. Observe the virtual dashboard’s real-time response to ECU CAN messages.  
6. Modify and extend the source code to experiment with CAN message handling and ECU behavior.  

---

## Future Improvements

- Extend support for AUTOSAR-compliant software components.  
- Implement advanced diagnostics and error handling features.  
- Optimize CAN message scheduling for enhanced real-time performance.  

---

## Author

**Saad Nm** — M.Sc. Automotive Software Engineering student  
[GitHub](https://github.com/SaadNjimi) 

---

*Feel free to contribute or reach out for collaboration!*
