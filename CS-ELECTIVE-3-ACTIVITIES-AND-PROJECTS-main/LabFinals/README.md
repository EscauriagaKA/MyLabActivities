# Final Project: Remote API LED Trigger System

## Description
The final project demonstrates an end-to-end IoT system. It utilizes an Arduino to detect a physical user interaction, which is then communicated via Serial to a Python middleware. This middleware processes the signal and executes a remote HTTP GET request to a FastAPI server on a different network to toggle a remote LED.

## Circuit Design
* **Inputs:** A push button connected to Digital Pin `2`.
* **Configuration:** Uses the `INPUT_PULLUP` mode, eliminating the need for an external resistor by utilizing the Arduino's internal pull-up resistor.
* **Outputs:** Status monitoring via the Serial Monitor.


## System Workflow & Logic
1. [cite_start]**Hardware (Arduino):** - Uses **Debounce Logic** to filter out mechanical noise from the button press[cite: 108].
   - [cite_start]When pressed, it sends a specific identifier (`GROUP_4`) through the Serial port[cite: 109, 110].
2. **Middleware (Python):**
   - Continuously monitors the Serial port for the group signal.
   - Upon receipt, it parses the group number and constructs a dynamic URL.
   - **Network Request:** Uses the `requests` library to target the API at `http://172.20.10.3:8000/led/group/4/toggle`.
3. **API (Remote Server):** Receives the request and toggles the corresponding LED on a separate system.

## Group Members & Grade
* Christian Lapidez — 100
* Emanuel Lloyd Dagdag — 100
* Jaye Dar Talili — 97
* John Paul Fidelson — 98
* Kyle Andrei Escauriaga — 100 (Leader)

## References
* [Python Requests Library Documentation](https://requests.readthedocs.io/)
* [Arduino Debounce Tutorial](https://www.arduino.cc/en/Tutorial/BuiltInExamples/Debounce)
