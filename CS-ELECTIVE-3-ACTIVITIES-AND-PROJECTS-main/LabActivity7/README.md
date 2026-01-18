# Laboratory Activity 7: IoT Integration via FastAPI

## Description
This activity demonstrates the integration of an Arduino system with a **Web API** using the **FastAPI** framework. It creates a bridge between web-based commands and physical hardware, allowing for remote monitoring and control of the system via a browser or HTTP client.

## Circuit Design
The hardware remains consistent with previous bidirectional setups but is now driven by a web server:
* [cite_start]**LEDs:** Red (7), Green (6), and Blue (5)[cite: 52, 53].
* [cite_start]**Buttons:** 3 Push buttons (12, 11, 10) set to `INPUT_PULLUP`[cite: 53, 56].

![Circuit Diagram](labact7diagram.png)

## Code Logic
The system architecture consists of two main parts:
1. **Web Server (`lab_act7.py`):**
   - Uses **FastAPI** to define endpoints like `/led/on`, `/led/off`, and `/led/{color}`.
   - When these URLs are accessed, the server writes specific characters ('1', '2', '3', or 'O') to the serial port.
   - It also provides a `/button/status` endpoint to read hardware events from the Arduino.
2. **Arduino Firmware (`lab_act7.ino`):**
   - [cite_start]**Serial Control:** Listens for characters from the FastAPI server to toggle LED states[cite: 57, 59, 61].
   - **Button Control:** Monitors physical buttons. [cite_start]When pressed, it toggles the local LED and sends a notification string (e.g., "BUTTON_RED") back to the web server[cite: 63, 65].

## Group Members & Grades
* **Leader:** Kyle Andrei Escauriaga
* **Members:**
    * Emanuel Lloyd Dagdag — 100
    * John Paul Fidelson — 98
    * Christian Lapidez — 99
    * Jaye Dar Talili — 97

## How to Run
1. Upload the `.ino` file to your Arduino Uno.
2. Install dependencies: `pip install fastapi uvicorn pyserial`.
3. Start the server: `uvicorn lab_act7:app --reload`.
4. Access `http://127.0.0.1:8000/led/red` to toggle the red LED via your browser.
