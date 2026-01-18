# Laboratory Activity 1: Working with Digital Signals 

## Description
This activity demonstrates the use of **Digital Signals** and **Control Structures** (specifically `for` loops) using an Arduino Uno. The program controls an array of 5 LEDs, sequentially turning them on one by one with a 1-second delay, and then turning them off in the same sequence.

## Circuit Design
The project uses the following components:
* Arduino Uno
* 5 LEDs connected to Digital Pins 12, 11, 10, 9, and 8
* Breadboard and jumper wires

![Circuit Diagram](LabAct1.jpg)

## Code Logic
1. **Initialization:** The LED pins are stored in an array and set as `OUTPUT` using a loop in the `setup()` function.
2. **Sequential On:** A loop iterates through the pins, setting each to `HIGH` with a 1000ms delay.
3. **Sequential Off:** A second loop iterates through the pins, setting each to `LOW` with a 1000ms delay.

## Group Members & Grades
* **John Paul Fidelson** (Leader)
* **Emanuel Lloyd Dagdag** — 97
* **Kyle Andrei Escauriaga** — 92
* **Christian Lapidez** — 100
* **Jaye Dar Talili** — 93

## References
* [Arduino For Loop Documentation](https://docs.arduino.cc/language-reference/en/structure/control-structure/for)
* Arduino Guide: Working with Analog and Digital Signals
