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

### TFT_eSPI

📦 Library Name in Library Manager: TFT_eSPI
🔗 TFT_eSPI on GitHub
📌 Note: You will need to configure User_Setup.h inside the library folder to match your display wiring and resolution (typically done once after installing the library).

### XPT2046_Touchscreen

📦 Library Name in Library Manager: XPT2046_Touchscreen
🔗 XPT2046_Touchscreen on GitHub
📌 Note: Used for touch input, compatible with SPI-based XPT2046 controllers.

### SPI

✅ Built-in with Arduino and ESP32 core
📌 No installation needed.

### Preferences

✅ Built-in with the ESP32 Arduino core
📌 Used for saving settings in non-volatile storage (like EEPROM).

### WiFi

✅ Built-in with ESP32 Arduino core
📌 Used to connect to WiFi networks.

### FS & SPIFFS (File System Support)

✅ Built-in with ESP32 Arduino core
📌 FS is a generic file system API; typically used with SPIFFS or LittleFS depending on your choice.
You may need to include or format your board with SPIFFS or LittleFS support, depending on what you use.

### WebServer

📦 Library Name in Library Manager: ESP32 WebServer (or comes with the ESP32 board support package)
📌 Provides a simple HTTP server.

### ESPmDNS

✅ Included with ESP32 Arduino core
📌 Enables mDNS (Multicast DNS), allowing your ESP32 to be reached via a name like etc.local instead of IP.

- Any other dependencies specific to your display or sensor setup

> ⚠️ Make sure you have selected the correct ESP32 board under **Tools > Board** in the Arduino IDE.

## 🔧 Setup

1. After downloaded change the code to your Wifi Settings

   ```bash
   Line 66 WiFi.begin("SSID Here", "Password here");
