Custom High-Performance Micro Drone Flight Controller
This repository documents the design and development of a feature-rich, custom 4-layer flight controller for a high-performance micro drone. The project's goal is to create a compact (<30x30mm), intelligent flight controller from scratch, capable of stable flight, autonomous navigation, and on-device AI/computer vision tasks.

Hardware Design
The hardware was designed from the ground up in EasyEDA, focusing on high performance, signal integrity, and a compact form factor. The 4-layer design incorporates dedicated inner planes for power and ground, ensuring a low-noise environment for the sensitive onboard sensors.

(Insert a screenshot of your final PCB Layout here)
![PCB Layout](https://github.com/prakash-not/MICRO-DRONE/blob/main/layout.png?raw=true)

(Insert a screenshot of your schematic here)
![Schematic](https://github.com/prakash-not/MICRO-DRONE/blob/main/schematic.png?raw=true)

Key Features & Components
This flight controller is packed with a suite of high-performance sensors and a powerful MCU to enable advanced features far beyond a typical micro drone.

Powerful Microcontroller: The ESP32-S3 serves as the core, providing dual-core processing power, Wi-Fi, and Bluetooth LE for control and data telemetry.

High-Performance IMU: An ICM-42688-P 6-axis IMU provides clean and stable motion data, which is critical for a locked-in flight feel.

Advanced Environmental Sensing: A BME680 sensor provides not only barometric pressure for altitude hold but also temperature, humidity, and air quality data.

Laser-Based Altitude Control: A VL53L0X Time-of-Flight laser rangefinder allows for incredibly accurate low-altitude position hold and automatic landings.

Efficient Power Electronics: Low Rds(on) IRLML6244 MOSFETs are used to drive the brushed motors, maximizing power delivery and efficiency.

Onboard AI/CV Ready: Includes a dedicated connector for an OV2640 camera module, enabling future development of on-device computer vision and AI tasks like gesture control or object tracking.

User Feedback: An addressable RGB LED (WS2812B) provides programmable visual status feedback (e.g., battery level, flight mode).

Component

Part Number

Function

Microcontroller

Seeed Studio Xiao ESP32-S3

Main Processor, Wi-Fi, BLE

IMU

TDK InvenSense ICM-42688-P

Motion Sensing (Gyro & Accel)

Barometer

Bosch BME680

Altitude, Temp, Humidity, Air Quality

ToF Sensor

STMicroelectronics VL53L0X

Laser Rangefinder for Altitude

MOSFETs

Infineon IRLML6244

Motor Drivers

RGB LED

WS2812B-Mini

Status Indicator

Software & Firmware (In Development)
The firmware is being developed in C++ using the ESP-IDF framework. The key software goals are:

Real-Time Control: Implement a robust PID control loop for stable, responsive flight.

Sensor Fusion: Develop algorithms to fuse data from the IMU, barometer, and ToF sensor for a highly accurate state estimation.

Wireless Control: Create a simple smartphone app that uses Bluetooth LE to control the drone.

Autonomous Modes: Program features like Altitude Hold, Position Hold, and Return to Home.

Computer Vision: Implement basic computer vision tasks using the OV2640 camera.

Current Status
[x] Hardware Design & Schematic: Complete

[x] PCB Layout & Routing (4-Layer): Complete

[x] Gerber File Generation: Complete

[ ] PCB Fabrication & Assembly: (Awaiting order)

[ ] Firmware Development: In Progress

[ ] Flight Testing & Tuning: (Pending hardware assembly)
