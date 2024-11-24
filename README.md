# CAS CHALLENGE PROJECT

An  application using the ESP32 microcontroller to monitor sensors (e.g., temperature, humidity, light intensity) and control actuators (e.g., servo motors, relays). The project integrates MQTT for remote communication and supports real-time monitoring and control.

## Features
- **Sensor Integration**:
  - Reads temperature and humidity using a DHT22 sensor.
  - Monitors light intensity and current using respective sensors.
- **Actuator Control**:
  - Controls servo motors, relays, and LEDs.
- **MQTT Communication**:
  - Publishes sensor data to specific MQTT topics.
  - Subscribes to actuator control commands via MQTT.
- **LCD Display**:
  - Displays sensor data and system status on an LCD screen.

## Hardware Requirements
- **Microcontroller**: ESP32
- **Sensors**:
  - DHT22 for temperature and humidity
  - Light sensor
  - Current sensor (ACS712)
  - Voltage sensor (ZMPT101B)
- **Actuators**:
  - Servo motor
  - Relay module
  - LEDs
- **Display**:
  - I2C LCD
- **Others**:
  - Wi-Fi-enabled network
  - MQTT broker (e.g., Mosquitto)

## Software Requirements
- Arduino IDE or PlatformIO
- Required libraries (install via Arduino Library Manager or PlatformIO):
  - PubSubClient
  - WiFi
  - DHT sensor
  - Servo
  - LiquidCrystal_I2C


## Installation and Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/esp32-iot-project.git
   cd esp32-iot-project
Configure the Project: Edit the src/config.h file to set your Wi-Fi and MQTT broker credentials:

cpp
Copier le code
#define WIFI_SSID "your-ssid"
#define WIFI_PASSWORD "your-password"

#define MQTT_SERVER "mqtt-broker-address"
#define MQTT_PORT 1883
#define MQTT_USER "mqtt-user"
#define MQTT_PASSWORD "mqtt-password"


Configure the Project: Edit the src/config.h file to set your Wi-Fi and MQTT broker credentials:

cpp
Copier le code
#define WIFI_SSID "your-ssid"
#define WIFI_PASSWORD "your-password"

#define MQTT_SERVER "mqtt-broker-address"
#define MQTT_PORT 1883
#define MQTT_USER "mqtt-user"
#define MQTT_PASSWORD "mqtt-password"
Upload the Code:

Open the project in Arduino IDE or PlatformIO.
Install required libraries.
Connect the ESP32 to your computer and upload the code.
Run the System:

Ensure the ESP32 is connected to Wi-Fi.
Start the MQTT broker and subscribe to relevant topics to monitor/control.
