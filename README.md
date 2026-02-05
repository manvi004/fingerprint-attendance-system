# Fingerprint Attendance System (ESP32)

This project implements a fingerprint-based attendance system
using an ESP32 microcontroller and a biometric fingerprint sensor.
The goal of the system is to automate attendance recording through
biometric authentication and log records remotely using IoT
services.

## System Overview

The system uses a fingerprint sensor to enroll and identify users
based on stored fingerprint templates. Once a fingerprint is
successfully matched, the ESP32 records the attendance event and
provides immediate feedback to the user through an LCD display.

Attendance data is transmitted over Wi-Fi and logged remotely
using IFTTT and Google Sheets.

## Fingerprint Authentication

The fingerprint sensor used in the system has internal memory
capable of storing up to 128 fingerprint templates. Enrollment,
deletion and matching of fingerprints are handled internally by
the sensor uses commands provided through the Adafruit
fingerprint library.

The ESP32 communicates with the sensor to:
* Enroll new fingerprints in a controlled enrollment mode
* Detect and match fingerprints during normal operation

## Attendance Logging

Upon successful fingerprint verification, the ESP32 sends the
attendance data to an IFTTT webhook. The IFTTT service then logs
the record into a Google Sheets document in real time. This
approach allows cloud-based attendance storage without the need
for a custom backend server.

## User Feedback

An I2C-based LCD module is used to display system messages such as
fingerprint status, attendance confirmation, and error messages.
This improves usability and provides immediate visual feedback
to users.

## Planned Upgrade

To improve scalability and long-term data management, the system
was later designed to support cloud server–based database storage.
In this approach, the ESP32 would transmit attendance data to a
server-side API, where records could be stored in a structured
database instead of a spreadsheet.

## Note

This repository documents the system architecture, working flow,
and design considerations. Firmware code is not included, as the
focus is on system-level integration and design rather than
library-based implementation.

The project was developed as part of undergraduate coursework
and focuses on embedded system integration, peripheral interfacing,
and cloud-based data logging.
