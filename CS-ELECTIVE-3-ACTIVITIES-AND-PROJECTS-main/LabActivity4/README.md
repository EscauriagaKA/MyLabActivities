# Laboratory Activity 4: Serial Communication and Interaction

## Description
This activity focuses on **Two-Way Serial Communication**. The system monitors temperature and triggers a visual alert (blinking LED) when a threshold is exceeded. Unlike previous activities, this project allows the user to interact with the running program by sending a text command through the Serial Monitor to silence the alert.

## Circuit Design
The setup utilizes an Arduino Uno with the following configuration:
* [cite_start]**Input:** A Thermistor connected to Analog Pin `A0` for environmental sensing.
* [cite_start]**Output:** An LED connected to Pin `8` for the alert signal.
* [cite_start]**Logic:** A pull-up resistor is used to create a voltage divider for accurate thermistor readings[cite: 26].

![Circuit Diagram](labact4diagram.png)

## Code Logic
1. [cite_start]**Non-Blocking Alert:** Instead of using `delay()`, this sketch uses `millis()` to handle the LED blinking[cite: 36]. This ensures the Arduino can still "listen" for user input while the LED is flashing.
2. [cite_start]**Threshold Logic:** If the temperature reaches **50.0°C**, the `isBlinking` state is set to `true`[cite: 34, 35].
3. **Serial Input Command:** The program constantly checks `Serial.available()`. [cite_start]If the user types **"stop"**, the program resets the alert state and turns off the LED[cite: 38, 41].

## Group Members & Grades
* **Leader:** Emanuel Lloyd Dagdag
* **Members:**
    * John Paul M. Fidelson
    * Kyle Andrei Escauriaga
    * Christian Lapidez
    * Jaye Dar Talili

## References
* [Arduino Millis() Documentation](https://www.arduino.cc/reference/en/language/functions/time/millis/)
* [Arduino Serial.readStringUntil()](https://www.arduino.cc/reference/en/language/functions/communication/serial/readstringuntil/)
