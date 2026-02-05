# Scalability Upgrade

While Google Sheets provides a convenient logging solution, it
has limitations in terms of scalability and structured data
management.

To address this, the system was designed to support a cloud
server–based database architecture. In this approach, the ESP32
would transmit attendance data to a backend service or API,
which would then store records in a database.

This design separates embedded data acquisition from the backend
storage and allows the system to scale beyond spreadsheet-based
logging.
