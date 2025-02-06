IoT-Based Temperature and Humidity Monitoring System

Overview

This project is an IoT-based temperature and humidity monitoring system using an ESP32, a DHT11 sensor, and the Adafruit MQTT platform. The system reads temperature and humidity data from the DHT11 sensor and publishes it to an Adafruit IO feed via MQTT. This allows real-time monitoring of environmental conditions remotely.

Features

Connects to a WiFi network for internet access

Reads temperature and humidity data from the DHT11 sensor

Publishes sensor data to Adafruit IO using MQTT

Reconnects automatically if the MQTT connection is lost

Provides serial monitor output for debugging

Components Used

ESP32 (or any compatible WiFi-enabled microcontroller)

DHT11 Sensor (for temperature and humidity measurement)

Adafruit IO (for data visualization and cloud storage)

Arduino IDE (for programming the ESP32)

Dependencies

Ensure you have the following libraries installed in the Arduino IDE:

WiFi.h (built-in for ESP32)

Adafruit MQTT Library (for MQTT communication)

DHT Sensor Library (for reading sensor data)

You can install these libraries via the Arduino Library Manager.

Setup and Configuration

Clone this repository:

git clone https://github.com/yourusername/your-repo-name.git

Open the project in the Arduino IDE.

Update the WiFi credentials in the code:

#define WLAN_SSID "your-SSID"
#define WLAN_PASS "your-PASSWORD"

Update Adafruit IO credentials:

#define AIO_USERNAME "your-username"
#define AIO_KEY "your-aio-key"

Upload the code to your ESP32.

Open the Serial Monitor (115200 baud rate) to check for connection logs.

How It Works

The ESP32 connects to the specified WiFi network.

It initializes the DHT11 sensor and starts reading temperature and humidity data.

The sensor data is published to Adafruit IO every 10 seconds.

The MQTT connection is maintained, and the device attempts to reconnect if disconnected.

Usage

Log in to Adafruit IO and navigate to your feeds.

Monitor the temperature and humidity values in real time.

Use the data for IoT applications such as automation, alerts, or dashboards.

Future Enhancements

Add support for more sensors (e.g., DHT22, BMP280)

Implement data logging for historical analysis

Enable alert notifications based on threshold values

Create a mobile app for real-time monitoring
