MediBox

MediBox is a smart pharmaceutical storage system designed to manage medicines effectively. This project focuses on the embedded software that controls the MediBox hardware, providing features such as medication reminders, environmental monitoring, and user interaction through a simple interface.


![image](https://github.com/user-attachments/assets/a822b704-b7bc-4998-8c06-725891121235)

Table of Contents
Introduction
System Overview
Prototype Overview
Functionalities
Advanced Functionalities
Software Architecture
Hardware Components
Installation
Usage
Contributing
License
Contact
Introduction
The MediBox Embedded Software Project develops a smart pharmaceutical storage system capable of managing medicines efficiently. This documentation outlines the design, implementation, and functionalities of the embedded software that controls the MediBox hardware components.

System Overview
MediBox integrates various hardware components, including an OLED screen, buzzer, push buttons, Light Dependent Resistors (LDRs), and a servo motor, all controlled by embedded software. Key features include:

NTP client for time synchronization.
Alarm management.
Temperature and humidity monitoring.
Light intensity monitoring.
User interface for interaction and configuration.
Prototype Overview

Functionalities
The MediBox software provides several core functionalities:

Time Management: Synchronize time with an NTP server and set a custom time zone.
Alarm Management: Set and manage medication alarms, including disabling alarms.
Environmental Monitoring: Monitor temperature, humidity, and light intensity, with visual and audible warnings.
User Interface: Display current time and system status on the OLED screen. Alarms can be acknowledged using push buttons.
Servo Motor Control: Adjust the shaded sliding window based on light intensity and user-defined parameters.
Advanced Functionalities
The MediBox software offers additional advanced features:

Persist alarm and user settings in non-volatile memory.
User-friendly OLED screen interface.
Power management system to reduce energy consumption.
Sensor "On Change Detection" to optimize performance.
Continuous monitoring of environmental factors with real-time data on the Node-RED dashboard.
Software Architecture
The MediBox software utilizes a modular architecture, ensuring clear separation of functionalities and easy maintenance:

Hardware Abstraction Layer (HAL): Simplifies the interaction with hardware components.
Sensor Management: Handles data acquisition from temperature, humidity, and light sensors.
Alarm Management: Enables medication reminders and stores configurations in non-volatile memory.
Time Management: Synchronizes time with the NTP server and allows for time zone customization.
User Interface: Provides a menu-driven interface on the OLED display for user interaction.
Communication Management: Establishes an MQTT connection for remote data transmission and control via Node-RED.
For more details on the architecture, see the Full Documentation.

Hardware Components
The hardware components of MediBox include:

ESP32 Development Board: The main controller, responsible for processing and connectivity.
OLED Display: Displays time, alarms, and system status.
Buzzer: Provides audible medication reminders.
Push Buttons: Allows user interaction for setting alarms and acknowledging notifications.
Light Dependent Resistors (LDRs): Monitors light intensity to control the shaded sliding window.
Servo Motor: Adjusts the window based on light intensity and user-defined parameters.
