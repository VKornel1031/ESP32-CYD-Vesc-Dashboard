# ESP32 CYD VESC Dashboard

An ESP32-based dashboard for VESC (Vedder Electronic Speed Controller) devices, designed for use with the CYD display. This project allows real-time monitoring of VESC data such as speed, voltage, current, and more, via WiFi.

## ✨ Features

- Real-time telemetry from VESC
- Display speed, voltage, current, and more
- Connects via WiFi to your VESC setup
- Designed for CYD displays using the ESP32

## ⚙️ Requirements

- **Hardware**
  - ESP32 (any dev board)
  - CYD Display
  - VESC (with UART or BLE telemetry output)
  
- **Software**
  - [Arduino IDE](https://www.arduino.cc/en/software)
  - Required Arduino Libraries (see below)

## 🧰 Libraries Required

Install the following libraries via the Arduino Library Manager:

- `WiFi.h`
- `VescUart`
- `TFT_eSPI`
- `ArduinoJson`
- Any other dependencies specific to your display or sensor setup

> ⚠️ Make sure you have selected the correct ESP32 board under **Tools > Board** in the Arduino IDE.

## 🔧 Setup

1. After downloaded change the code to your Wifi Settings

   ```bash
   Line 66 WiFi.begin("SSID Here", "Password here");
