# 🌿 xiao-soil-moisture-esphome - Keep your plants healthy with ease

[![](https://img.shields.io/badge/Download-Latest_Release-blue.svg)](https://github.com/sternwelltimed533/xiao-soil-moisture-esphome)

This project provides firmware for the Seeed XIAO ESP32-C6 soil moisture sensor. The software allows the sensor to run for nearly two years on a single AA battery. It sends moisture data to your home automation system so you know exactly when to water your plants.

## ⚙️ System Requirements

To use this software, you need the following items:

* A computer running Windows 10 or 11.
* A Seeed XIAO ESP32-C6 board.
* A USB-C cable to connect the board to your computer.
* A AA battery and a suitable holder.
* A soil moisture sensor probe.
* An existing Home Assistant setup or an MQTT broker.

## 📥 Get the Software

You must visit the project page to access the installation files. The software includes the base firmware and the necessary configuration files to get your sensor running.

[Download the latest firmware files here](https://github.com/sternwelltimed533/xiao-soil-moisture-esphome)

Click the link above to reach the main page. Look for the section labeled "Releases" on the right side of the screen. Click the most recent version number to view the available files. Download the file ending in `.bin` to your computer.

## 🛠️ Prepare Your Hardware

Connect the Seeed XIAO ESP32-C6 to your computer using the USB-C cable. Windows should recognize the board automatically. If your computer asks for drivers, download the standard CH340 or CP210x driver from the Seeed Studio website. 

Ensure your cable supports data transfer. Some cables only provide power and will not allow you to update the firmware.

## 🚀 Install the Firmware

1. Open your web browser and navigate to the [ESPHome Web Flasher](https://web.esphome.io/).
2. Click the Connect button on the website.
3. Select the port that corresponds to your XIAO board from the list. 
4. Click the Install button.
5. Choose the file you downloaded earlier from your computer.
6. Wait for the progress bar to complete. The board will restart once the process finishes.

## 📶 Connect to Your Network

Once the firmware installation finishes, the board creates a temporary wireless network. Use your smartphone or computer to find a network named "ESPHome". 

1. Connect to the "ESPHome" network.
2. A window should pop up automatically. If it does not, open a web browser and type `192.168.4.1` into the address bar.
3. Enter your home wireless network name (SSID) and password.
4. Click Save. 

The sensor will now reboot and attempt to connect to your home network.

## 📊 View Your Data

The sensor reports moisture levels every few hours to save power. If you use Home Assistant, the device will appear automatically under your "Devices & Services" menu. You can add the sensor to your dashboard to monitor soil levels in real time. 

If you use a different system, the sensor publishes data to an MQTT topic. You can view these messages using any standard MQTT client.

## 🔋 Optimize Battery Life

The deep-sleep mode allows the sensor to remain active for up to 600 days. Do not remove the battery unless you need to turn the device off for a long period. If the sensor stops reporting, replace the AA battery with a fresh one. 

The Seeed XIAO ESP32-C6 manages its power consumption automatically. You do not need to adjust any settings to enable the low-power features. The firmware handles the deep-sleep cycles on its own.

## ❓ Common Issues

* **The board does not appear in the flasher:** Check that your USB cable is plugged in securely. Try a different USB port on your computer.
* **The device does not connect to Wi-Fi:** Ensure your network uses a 2.4GHz frequency. These devices cannot connect to 5GHz networks.
* **Data does not update:** Wait for the next reporting interval. The device spends most of its time in sleep mode to conserve battery. 
* **Sensor readings look wrong:** Check the connection between the probe and the board. Ensure the probe pins are clean and pushed firmly into the soil.

Keywords: battery-powered, deep-sleep, esp32, esp32c6, esphome, firmware, gardening, home-assistant, homeassistant, iot, low-power, mqtt, plant-monitoring, seeed-studio, smart-garden, soil-moisture, soil-moisture-sensor, xiao