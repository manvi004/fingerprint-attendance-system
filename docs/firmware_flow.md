# ESP32 Firmware Flow (Pseudocode)

This document outlines the logical flow of the ESP32 firmware
used in the fingerprint attendance system. The actual firmware
implementation is not included, as it relies on standard library
functions and was developed as part of a group project.

## Initialization
1. Initialize serial communication
2. Initialize fingerprint sensor
3. Initialize LCD 
4. Connect to Wi-Fi network

## Enrollment Mode
1. Trigger enrollment mode through a controlled input
2. Capture fingerprint data
3. Store fingerprint template in sensor memory
4. Display enrollment status on LCD

## Attendance Mode
1. Wait for finger placement
2. Request a fingerprint match from the sensor
3. If a match is found:
* Retrieve fingerprint ID
* Display attendance confirmation on LCD
* Send attendance data to the IFTTT webhook
4. If no match is found, then display an error message on the LCD

## Idle State
System remains in attendance mode until reset or reconfigured
