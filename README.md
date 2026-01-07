# wmbus_json_serializer

## Overview
This project implements a JSON serializer for Wireless M-Bus (wMBus) meter data using ESP-IDF and C language.

The goal is to convert structured meter data (meter ID, meter type, timestamp, and measurements) into a JSON formatted string suitable for transmission or logging.

This implementation is hardware-independent and focuses on data serialization logic.

## Project Structure
wmbus_json_serializer/
├── CMakeLists.txt
├── sdkconfig
├── expected_output.json
├── main/
│   ├── CMakeLists.txt
│   ├── main.c
│   ├── wmbus_json.c
│   └── wmbus_json.h

## How It Works
- `main.c` creates a sample meter data structure.
- The data is passed to `wmbus_meter_to_json()`.
- `wmbus_json.c` converts the structure into a JSON string using `snprintf`.
- The generated JSON matches the format shown in `expected_output.json`.

## Expected Output
See `expected_output.json` for the sample JSON produced by this project.

## Build Environment
- ESP-IDF v5.x
- Language: C
- Platform: ESP32 (logic is platform-independent)

## Notes
No ESP32 hardware is required to understand or review this project.
