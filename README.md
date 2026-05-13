# I2C Scanner for Arduino

## Overview

This project is a simple I2C scanner for Arduino-compatible boards. It scans all possible I2C addresses and prints the detected devices to the Serial Monitor.

The program is especially useful when working with I2C modules whose address is unknown, such as OLED displays, sensors, RTC modules, EEPROMs, or I/O expanders.

## Features

- Scans the full I2C address range from `0x01` to `0x7E`
- Prints detected I2C device addresses in hexadecimal format
- Reports unknown I2C communication errors
- Uses custom SDA and SCL pins
- Repeats the scan every 5 seconds

## Hardware Requirements

- Arduino-compatible board
- One or more I2C devices
- Jumper wires
- USB cable for Serial Monitor connection

## Pin Configuration

The I2C bus is initialized with the following pins:

| Signal | Pin |
|------:|----:|
| SDA | 20 |
| SCL | 21 |

```cpp
Wire.begin(20, 21);
