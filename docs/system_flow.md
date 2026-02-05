# System Flow

The system operates in two primary modes: enrollment mode and
attendance mode.

## Enrollment Mode
Enrollment is a controlled process used to register new users.
In this mode, the ESP32 instructs the fingerprint sensor to store
a new fingerprint template in its internal memory. This mode is
typically triggered through a serial command or a dedicated
control mechanism.

## Attendance Mode
During normal operation, the system remains in attendance mode.
When a user places a finger on the sensor, the fingerprint is
matched against stored templates.

If a match is found:
1. The fingerprint ID is returned to the ESP32
2. Attendance is marked
3. Data is sent to the cloud for logging
4. Status is displayed on the LCD

If no match is found, the system displays an appropriate message
and no data is logged.
