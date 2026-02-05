# Attendance Data Logging

Attendance records are logged using an IoT-based approach. Upon
successful fingerprint authentication, the ESP32 sends attendance
data to an IFTTT webhook using an HTTP request.

The IFTTT service processes this request and appends the data
to a Google Sheets document. This method provides a simple and
accessible way to store attendance records without maintaining
a custom backend or database.

