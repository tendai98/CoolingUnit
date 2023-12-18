
# 🌬️Cooling Unit Implementation with ESP8266 Controller and Peltier Elements 🌡️

## Overview ℹ️

This project involves the implementation of a cooling unit utilizing an ESP8266 controller and Peltier heating and cooling elements. It aims to regulate temperature by controlling the Peltier elements based on predefined temperature thresholds.

## Structure 📁

```
- CoolingUnit.ino
- dht.h
- oled.h
- README.md
- relay.h
- server.h
```

## Code Overview 💻

### CoolingUnit.ino

The main code file `CoolingUnit.ino` integrates functionalities from different header files to execute the cooling unit's operation. It orchestrates the following tasks:

- Initializes various components (sensors, OLED display, networking, and relays) in the `setup()` function.
- Manages a continuous loop (`loop()`) that performs the following:
  - Runs a server to handle system states and reset commands.
  - Displays temperature and humidity readings on the OLED screen.
  - Controls the relay based on temperature thresholds for Peltier element activation.

### dht.h (Temperature and Humidity Sensor) 🌡️

This header file implements the sensor-related functionalities:

- Utilizes the DHT library to handle temperature and humidity readings from the DHT11 sensor.
- Functions such as `initSensor()`, `getTemperature()`, and `getHumidity()` manage sensor initialization and data retrieval.

### oled.h (OLED Display) 🖥️

Handles the OLED display functionalities:

- Initializes and operates the OLED display using the U8g2 library.
- Functions like `initOLED()`, `displayTopRow()`, and `displayBottomRow()` manage OLED content display.

### relay.h (Relay Control) ⚡

Manages the relay control functionalities for the Peltier elements:

- Initializes relay pins and controls relay states (`switchRelay()` function) for both the fan and the Peltier element.

### server.h (Web Server) 🌐

Implements a basic web server using the ESP8266WebServer library:

- Initializes an HTTP server and defines routes (`/state` and `/reset`) to retrieve system states and perform system resets, respectively.
- Functions like `initNet()`, `initServer()`, `runServer()`, `getSystemState()`, and `resetSystem()` handle networking and server operations.

## Usage 🛠️

This repository contains code segments for a cooling unit project designed for educational purposes. To execute or replicate the functionalities, load the provided code into an ESP8266-compatible development environment, ensure proper hardware connections, and upload the code onto the ESP8266 controller. Detailed hardware setups and connections might be required based on the code segments provided.
