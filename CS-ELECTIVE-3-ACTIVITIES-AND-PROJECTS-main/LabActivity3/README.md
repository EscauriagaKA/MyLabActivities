# Laboratory Activity 3: Working with Sensors (Fire Detection System)

## Description
This activity demonstrates the integration of multiple analog sensors to create a conditional alert system. The system simulates a **Fire Detector** by simultaneously monitoring ambient temperature and light levels.

## Circuit Design
The system uses an Arduino Uno to interface with:
* [cite_start]**Input Sensors:** A Thermistor (Temperature)  [cite_start]and a Photoresistor (Light)[cite: 11].
* [cite_start]**Output Actuator:** A combined LED and Buzzer alert pin (Pin 12).
* **Setup:** Components are wired using a pull-up resistor configuration to ensure accurate analog readings.

![Circuit Diagram](LabAct3Diagram.jpg)

## Code Logic
1. [cite_start]**Environmental Monitoring:** - The system reads analog values from the Thermistor (`A0`) and Photoresistor (`A2`).
   - [cite_start]**Temperature Calculation:** Uses the Steinhart-Hart Equation to convert raw analog data into Celsius[cite: 14].
2. [cite_start]**Conditional Alert:** - The system checks if both thresholds are met: Temperature $\ge 50.0^\circ\text{C}$ AND Brightness $\ge 220$[cite: 10, 11, 22].
3. [cite_start]**Response:** - If a fire is detected, the `ALERT_PIN` triggers a fast-pulsing sequence (50ms) to drive both the LED and Buzzer[cite: 22, 23].
   - [cite_start]Otherwise, the system remains in a "Normal" state with the alert pin `LOW`[cite: 24].

## Group Information and Grade
* **Leader:** Christian L. Lapidez
* **Members:**
    * Emanuel Lloyd Dagdag — 92
    * Kyle Andrei Escauriaga — 95
    * Jaye Dar Talili — 94
    * John Paul Fidelson — 93

## Reference / Citation
* **YouTube:** [Thermistor Wiring Guide](https://www.youtube.com/watch?v=jmva62r8KUU)
* **Laboratory Manual:** *Working with Sensors* (PDF)
