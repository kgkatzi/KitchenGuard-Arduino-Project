# KitchenGuard-Arduino-Project
Developed a sensor network using Arduino to prevent kitchen accidents, demonstrating practical application of embedded systems

# README for KitchenGuard System

## Overview

The KitchenGuard system comprises two components: the Detector (transmitter) and the Notifier (receiver). The Detector monitors various environmental factors in the kitchen, such as temperature, gas levels, flame presence, and humidity, to detect potential hazards like water boiling, gas leaks, fires, and water leaks. When a hazard is detected, the Detector sends a status message to the Notifier, which displays corresponding alerts on an LCD screen and generates audible notifications.

## Detector (Transmitter)

### Modules Used
- **RF22 Library**: Used for wireless communication between the Detector and Notifier.
- **DHT Library**: Enables communication with the DHT11 humidity and temperature sensor.
- **Waveshare_LCD1602_RGB Library**: Controls the Waveshare LCD display.
- **LiquidCrystal Library**: Alternative library for LCD display (commented out in the code).

### Components
- **Force Sensor**: Monitors force (pot presence) in the kitchen.
- **Gas Sensor**: Detects gas levels in the kitchen.
- **Flame Sensor**: Detects the presence of flames.
- **DHT11 Humidity and Temperature Sensor**: Measures humidity and temperature.
- **LCD Display**: Shows real-time status information.
- **RF22 Transceiver**: Facilitates wireless communication with the Notifier.

### Operation
1. The Detector continuously monitors environmental factors.
2. When a hazard is detected (e.g., water boiling, gas leak, fire, water leak), it sends a status message to the Notifier using RF22 wireless communication.
3. The LCD display on the Detector provides real-time status information.

## Notifier (Receiver)

### Modules Used
- **RF22 Library**: Used for wireless communication between the Detector and Notifier.
- **Waveshare_LCD1602_RGB Library**: Controls the Waveshare LCD display.

### Components
- **Buzzer**: Generates audible alerts.
- **LCD Display**: Shows real-time alerts and status information.

### Operation
1. The Notifier listens for status messages from the Detector using RF22 wireless communication.
2. Upon receiving a message, it interprets the status and displays corresponding alerts on the LCD.
3. Audible alerts are generated based on the type of hazard detected.

## Status Codes
- **0**: Everything is okay.
- **1**: Water boiling with pot.
- **2**: Water boiling without pot.
- **3**: Gas leak.
- **4**: Fire.
- **5**: Water leak.
- **6**: Issue with the device.

## How to Use

1. Set up the hardware components as specified in the code.
2. Upload the Detector code to the Detector module.
3. Upload the Notifier code to the Notifier module.
4. Ensure both modules are powered and have a wireless communication link.
5. Monitor the LCD display on the Notifier for real-time alerts.

Feel free to modify the code and hardware configurations to suit your specific requirements. Adjust thresholds, sensor placements, and alert mechanisms based on your kitchen environment.
