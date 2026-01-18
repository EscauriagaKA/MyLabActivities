# Laboratory Activity 2: Working with Analog Signals 

## Description
This activity explores **Analog Signals** and **PWM (Pulse Width Modulation)**. Unlike the first activity which was strictly binary (HIGH/LOW), this sketch uses `analogWrite()` to create a "fading" or "breathing" effect by gradually increasing and decreasing the voltage sent to the LEDs.

## Circuit Design
The circuit expands on the previous setup by utilizing PWM-capable pins on the Arduino Uno:
* **Components:** 5 LEDs, 1 Potentiometer (as seen in the diagram), and an Arduino Uno.
* **Connections:** LEDs are connected to pins 8, 9, 10, 11, and 12.

![Circuit Diagram](labact2diagram.png)

## Code Logic
1. **Brightness Control:** The code uses nested `for` loops to iterate through a brightness range of 0 to 255.
2. **Fade In:** Each LED gradually brightens as the `brightness` variable increases, using `analogWrite(ledPins[i], brightness)`.
3. **Fade Out:** A second loop decreases the brightness from 255 down to 0 to create the fading effect.
4. **Timing:** A short `delay(5)` creates a smooth visual transition.

## Group Information and Grade
* **Leader:** Jaye Dar Talili
* **Members:**
    * Emanuel Lloyd Dagdag — 83
    * Kyle Andrei Escauriaga — 82
    * Christian Lapidez — 85
    * John Paul Fidelson — 84

## Reference / Citation
* **Generative AI:** ChatGPT (Model: GPT-4o) used to clarify the `map()` function for future implementation.
* **Documentation:** *Arduino Guide: Working with Analog and Digital Signals*, Page 3.
