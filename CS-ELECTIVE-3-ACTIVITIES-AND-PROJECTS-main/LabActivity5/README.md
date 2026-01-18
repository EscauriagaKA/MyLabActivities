# Laboratory Activity 5: Serial Control via Python

## Description
This activity demonstrates **Inter-system Communication** by using a Python script to send commands to an Arduino Uno over a serial connection. This project simulates a simple "Smart Home" lighting control system where the user interacts with a CLI (Command Line Interface) on their computer to toggle physical LEDs.

## Circuit Design
The hardware setup involves an Arduino Uno connected to three distinct LEDs representing different zones or states:
* **Red LED:** Pin 8
* **Green LED:** Pin 9
* **Blue LED:** Pin 10
* **Configuration:** Each LED is connected through a current-limiting resistor to protect the components.

![Circuit Diagram](lab_act5_diagram.png)

## Code Logic
The project is split into three functional parts:
1. **Python Menu (`lab_act5.py`):** Provides a user-friendly interface using the `pyserial` library to encode character commands ('R', 'G', 'B', etc.) and send them to the COM port.
2. **Arduino Sketch (`lab_act5.ino`):** Listens for incoming serial bytes. When a byte is received, it passes it to the processing function.
3. **Header Logic (`lab_act5.h`):** Contains the `processCommand()` function which uses a `switch` statement to toggle the appropriate LED state or trigger the "All ON/OFF" functions.

## Group Information and Grade
* **Leader:** Emanuel Lloyd Dagdag
* **Members:**
    * John Paul Fidelson
    * Kyle Andrei Escauriaga
    * Christian Lapidez
    * Jaye Dar Talili

