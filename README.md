# Embedded systems: ESP8266 door access control

> **TL;DR:** A distributed access-control prototype using three ESP8266 nodes, RFID, a keypad and MQTT. My contribution centered on hardware schematics, separating components across boards and prototyping output controls.

## My contribution - Alfred Aqraou

- Updated Fritzing schematics and split the hardware across boards when the keypad exceeded the available pins.
- Added and documented hardware components including an active buzzer, RGB light and potentiometer.
- Exported circuit diagrams and contributed an initial script for the third ESP8266 node's outputs.

This was a group project with Mathias K. E. Sørensen, Hector Foss and Nikolaj. The full firmware and MQTT system were developed collaboratively; the bullets identify my own recorded work.

**Original team repository:** [MathiasKES/34338-Project](https://github.com/MathiasKES/34338-Project). This portfolio fork preserves the original history and attribution.

**Selected contributions:** [Keypad board split](https://github.com/MathiasKES/34338-Project/commit/42974b9167d9e1b6fb901693f00aa6e562744678) · [Buzzer and RGB light](https://github.com/MathiasKES/34338-Project/commit/3aeaeb25cf7d3cfa2a2e1e16437de29c6ffa4b2a) · [Schematics and output prototype](https://github.com/MathiasKES/34338-Project/commit/67a58d45345c2a416c3cb601a3c4c2cbe71d939e).

---

## Project documentation

This project implements a distributed door access control system using
multiple ESP8266 nodes communicating over MQTT.

## System Overview

The system consists of three ESP8266 nodes:

- **ESP1 – RFID & Motion**
  Handles RFID authentication, LCD feedback, and motion sensing.

- **ESP2 – Keypad**
  Handles PIN entry and reports keypad interaction.

- **ESP3 – Door Actuator**
  Controls the door lock servo, LEDs, and buzzer.

A shared `WiFiMqttClient` library provides a unified abstraction for
WiFi and MQTT communication.


The pin maps of ESP2866MOD: 
https://lastminuteengineers.com/esp8266-pinout-reference/

## Doxygen
The homepage of doxygen can be accessed:
**[Locally](docs/html/index.html)**
or
**[Remotely](https://mathiaskes.github.io/34338-Project/html/)**