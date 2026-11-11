ESP32 PIR Motion Detection System

An automatic motion detection and light control system using ESP32, PIR motion sensor, and a relay module.

This project detects human movement using a PIR sensor and automatically turns ON a connected light through a relay. When no further motion is detected, the light automatically turns OFF after 10 seconds.

Features

- PIR-based motion detection
- Automatic light ON/OFF control
- 10-second automatic light-off timer
- Active-LOW relay control
- 15-second PIR sensor calibration
- Real-time Serial Monitor status
- Simple and beginner-friendly Arduino code

Hardware Requirements

Component| Quantity
ESP32 Development Board| 1
PIR Motion Sensor (HC-SR501)| 1
1-Channel Relay Module| 1
Jumper Wires| As required
Light / Bulb| 1

Circuit Connections

Component| ESP32 GPIO
PIR Sensor OUT| GPIO 27
PIR Sensor VCC| 5V (as supported by module)
PIR Sensor GND| GND
Relay IN| GPIO 26
Relay VCC| As supported by module
Relay GND| GND

Working Principle

1. The ESP32 starts and initializes the PIR sensor and relay.
2. The PIR sensor gets 15 seconds to calibrate.
3. When motion is detected, the relay turns ON the light.
4. Every new motion detection resets the 10-second timer.
5. If no further motion is detected for 10 seconds, the relay turns OFF the light.
6. The system continuously monitors motion.

Software Requirements

- Arduino IDE
- ESP32 Board Package
- No additional libraries required

Configuration

You can modify these settings in the source code:

#define PIR_PIN 27
#define RELAY_PIN 26

#define RELAY_ON LOW
#define RELAY_OFF HIGH

const unsigned long LIGHT_ON_TIME = 10000;

Change the light duration:

- 5 seconds: "5000"
- 10 seconds: "10000"
- 30 seconds: "30000"
- 60 seconds: "60000"

Serial Monitor Output

ESP32 PIR Motion Detection System
PIR Sensor Calibrating...
System Ready!
Waiting for Motion...

Motion Detected!
Light ON

Light OFF

Applications

- Automatic room lighting
- Smart home automation
- Motion-activated security lighting
- Energy-saving lighting systems
- DIY IoT projects

Safety Notice

For AC mains-powered lights, use a properly rated relay module and insulated electrical connections. Never touch exposed mains wiring while powered. Seek qualified assistance for AC wiring.

Creator

Technical BD
YouTube:https://youtube.com/@technicalbdvrj?si=dWCdxQavmbprNWBA
Project Video:https://youtu.be/iRx-G59B7ig

If you find this project useful, consider giving this repository a ⭐ Star.

Made with ESP32 | Arduino | DIY Electronics | IoT
