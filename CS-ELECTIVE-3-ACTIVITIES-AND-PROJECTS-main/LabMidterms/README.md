# Midterm Project: Intelligent Light Level Controller

## Description
This project implements a multi-mode light monitoring system that reacts to environmental light levels using a photoresistor. It demonstrates sophisticated state management by allowing the user to toggle between preset "Automatic" behaviors and customizable "Manual" thresholds via serial commands.

## Circuit Design
* [cite_start]**Sensors:** Photoresistor (LDR) connected to Analog Pin `A0`[cite: 66].
* [cite_start]**Indicators:** Three LEDs (Red, Yellow, Green) representing different intensity zones[cite: 66].
* **Setup:** A voltage divider circuit is used to convert the variable resistance of the LDR into a readable analog voltage.


## Code Logic & Features
1. **Operating Modes:**
   - [cite_start]**Automatic Mode:** Uses fixed thresholds (40% and 70%) to categorize the environment as "Cloudy" or "Clear"[cite: 69, 70, 79, 80].
   - [cite_start]**Manual Mode:** Allows users to define their own custom LOW and HIGH thresholds during runtime[cite: 68, 89, 93].
2. **Serial Command Interface:**
   - [cite_start]`MODE AUTO` / `MODE MANUAL`: Switches the system's operational logic[cite: 87, 88].
   - [cite_start]`SET LOW xx` / `SET HIGH xx`: Dynamically updates threshold variables in Manual mode[cite: 89, 93].
3. [cite_start]**Data Normalization:** The system maps raw analog input (0-1023) to a human-readable percentage (0-100%) for more intuitive monitoring[cite: 78].

## Group Members & Grade
* [cite_start]Christian Lapidez — 100 [cite: 51]
* [cite_start]Emanuel Lloyd Dagdag — 96 [cite: 51]
* [cite_start]Jaye Dar Talili — 98 [cite: 51]
* [cite_start]John Paul Fidelson [cite: 51]
* [cite_start]Kyle Andrei Escauriaga — 97 [cite: 51]

## References
* [Arduino Map() Function](https://www.arduino.cc/reference/en/language/functions/math/map/)
* [Voltage Divider Theory](https://learn.sparkfun.com/tutorials/voltage-dividers/all)
