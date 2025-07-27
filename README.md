# ESP32 Incubator Monitoring System

An IoT-based monitoring system for incubator environments using ESP32 microcontroller. Tracks vital environmental and physiological parameters with real-time data logging and wireless connectivity.

## Key Features

- **Environmental Monitoring**: Temperature, humidity, and pressure sensing
- **Health Monitoring**: Heart rate and SpO2 measurement
- **Sound Level Detection**: Ambient noise monitoring
- **Real-time Display**: OLED display for live sensor readings
- **Data Logging**: SD card storage with timestamp logging
- **Wireless Connectivity**: WiFi-enabled with cloud integration
- **Alarm System**: Configurable thresholds with alerts

## Technology Stack

- **Platform**: PlatformIO, Arduino Framework
- **Hardware**: ESP32, BME280, MAX30102, MAX4466, SSD1306 OLED, SD Card
- **Connectivity**: WiFi, ThingSpeak IoT platform
- **Libraries**: Adafruit sensors, SparkFun MAX3010x, NTPClient

## Project Structure

```
├── src/main.cpp              # Main application code
├── dev/                      # Development and testing files
│   ├── bme280-*.cpp         # BME280 sensor experiments
│   ├── max30102-hr.cpp      # Heart rate sensor testing
│   └── sensors-oled*.cpp    # Combined sensor implementations
└── platformio.ini           # Project configuration
```

## Technical Skills Demonstrated

- Embedded systems programming (C++/Arduino)
- Multi-sensor data acquisition and filtering
- Real-time data processing and averaging algorithms
- IoT connectivity and cloud data transmission
- File system management and data logging
- Hardware integration and pin configuration

---

*Developed for demonstrating embedded systems, IoT, and real-time monitoring capabilities.*