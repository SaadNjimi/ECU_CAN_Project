ECU_CAN_Project
Overview
This project demonstrates the development of an Electronic Control Unit (ECU) application with CAN bus communication, implemented as part of a university automotive software engineering course. The ECU interacts with a virtual dashboard simulator (VirtualCockpit) by sending and receiving CAN messages to control vehicle indicators such as speed, RPM, and lights.

Features
CAN controller configuration for message transmission and reception (standard and extended frames).

Message filtering based on CAN IDs (0x10, 0x11).

Interrupt-driven message handling with LED indicators.

Periodic sending of CAN messages to control virtual dashboard elements:

Vehicle speed mapped from an analog potentiometer input (0–240 km/h).

Cyclic RPM pattern generation.

Lights and indicators control based on input switches.

Integration and validation with the VirtualCockpit tool for real-time simulation.

Technologies & Tools
Programming Language: C (Embedded)

Hardware: Microcontroller with CAN Bus support

Software Tools: VirtualCockpit (dashboard simulator), CAN protocol stack

Project Structure
source/siu.c — CAN controller pin configuration and initialization

source/can.c — CAN message buffer setup and transmission functions

main.c — Main program flow, message handling, and LED control

Additional headers and configuration files for CAN filtering and buffer management

How to Use
Set up the microcontroller hardware and connect to the CAN bus.

Launch the VirtualCockpit tool on the development PC.

Compile and flash the ECU firmware.

Use VirtualCockpit to send “Start Engine” (ID 0x11) and “Stop Engine” (ID 0x10) messages.

Observe the virtual dashboard reacting to CAN messages sent from the ECU.

Modify the source code to experiment with different CAN message behaviors and configurations.

Future Work
Extend support for AUTOSAR-compliant software components.

Implement advanced diagnostics and error handling.

Optimize CAN message scheduling for real-time performance.

Author
Saad Njimi — M.Sc. Automotive Software Engineering student

