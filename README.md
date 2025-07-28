# ESP32 Incubator Monitoring System

ESP32-based monitoring system for incubator environments using multiple sensors.

The system monitors:
- Temperature and humidity (BME280)
- Heart rate (MAX30102)
- Sound levels (MAX4466)
- Data logging to SD card
- Wireless data upload to ThingSpeak

## Hardware

- ESP32 development board
- BME280 environmental sensor
- MAX30102 pulse oximeter
- MAX4466 microphone module
- SSD1306 OLED display
- SD card module

## Libraries

```
Adafruit GFX Library
Adafruit SSD1306
Adafruit BME280 Library
Adafruit BusIO
SparkFun MAX3010x Pulse and Proximity Sensor Library
ThingSpeak
Time
NTPClient
```

Install via PlatformIO: `pio lib install`

## Configuration

1. Update WiFi credentials in `main.cpp`:
   ```cpp
   const char* SSID = "your_wifi_name";
   const char* PASSWORD = "your_password";
   ```

2. Set ThingSpeak API key:
   ```cpp
   const char* WRITE_API_KEY = "your_api_key";
   ```

## Usage

```bash
pio run --target upload
pio device monitor
```

The system displays real-time data on the OLED and uploads to ThingSpeak every 20 seconds.

## Development Files

The `dev/` folder contains individual sensor test files:
- `bme280.cpp` - Temperature/humidity only
- `max30102-hr.cpp` - Heart rate only  
- `max4466.cpp` - Sound level only
- `sensors-oled.cpp` - Combined sensors with display
- `sensors-oled-wireless.cpp` - Adds wireless upload
- `sensors-oled-wireless-logging.cpp` - Full system with SD logging
