Walgama Kankanamge Praveen Kavishka
4230z
Kaveen Dulaj Adithya Fernando
4230z


Smart Clothes Drying System Using Arduino
Project Title

IoT Smart Clothes Drying System with Rain Detection

Description

This project demonstrates a smart home automation system using an Arduino microcontroller and environmental sensors. The system automatically protects clothes from rain by detecting weather conditions and controlling a protective cover.

The purpose of this project is to create a practical automation system that helps with daily household tasks such as drying clothes safely outdoors without worrying about sudden rain.

The system uses sensors to detect rain, humidity, and sunlight conditions. When rain is detected, the system automatically closes a cover to protect the clothes. When the weather becomes sunny again, the cover opens so the clothes can continue drying.

This system can be used in homes, apartments, balconies, and smart-city residential buildings where outdoor clothes drying is common.

Components
Arduino Uno
Rain Sensor Module
DHT11 Humidity Sensor
LDR Light Sensor
Servo Motor (Automatic Cover Control)
ESP8266 WiFi Module
Breadboard
Jumper wires
Power supply / USB cable
Circuit Diagram

Connections used in the project:

Rain Sensor:

VCC → Arduino 5V
GND → Arduino GND
OUT → Arduino Pin 2

DHT11 Humidity Sensor:

VCC → Arduino 5V
GND → Arduino GND
DATA → Arduino Pin 4

LDR Light Sensor:

One pin → Arduino A0
Other pin → GND

Servo Motor:

VCC → Arduino 5V
GND → Arduino GND
Signal → Arduino Pin 9

ESP8266 WiFi Module:

VCC → 3.3V
GND → GND
TX → Arduino RX
RX → Arduino TX
Code
#include <Servo.h>

int rainPin = 2;
int lightSensor = A0;
Servo cover;

void setup() {
  pinMode(rainPin, INPUT);
  cover.attach(9);
}

void loop() {

  int rain = digitalRead(rainPin);
  int lightValue = analogRead(lightSensor);

  if (rain == LOW) {
    cover.write(0);   // close cover
  }
  else if (lightValue > 600) {
    cover.write(90);  // open cover
  }

  delay(500);
}
Weekly Updates
Week 1 – INTRO (06/03/2026)
Selected Project Topic

The selected project is Smart Clothes Drying System using Arduino. This project focuses on creating a smart system that automatically protects clothes from rain.

Project Idea

The idea of the project is to use rain, humidity, and sunlight sensors with an Arduino Uno to monitor weather conditions. When rain is detected, the system will automatically close a protective cover over the clothes. When the weather becomes sunny again, the cover will open automatically.

This system helps improve convenience and prevents clothes from getting wet due to unexpected rain.

Project Objectives
To learn the basics of Arduino and sensors
To build a smart home automation system
To detect rain using a rain sensor
To automatically protect clothes using a motorized cover
Components Required
Arduino Uno
Rain Sensor Module
DHT11 Humidity Sensor
LDR Light Sensor
Servo Motor
ESP8266 WiFi Module
Breadboard
Jumper wires
USB cable
Week 2 – BASICS (20/03/2026)
Building the Basic Circuit

The basic circuit was created by connecting the rain sensor, light sensor, and servo motor to the Arduino Uno using a breadboard. The rain sensor detects rain and sends a signal to the Arduino controller.

Implementing the Arduino Code

The Arduino program was written to read the sensor values. When rain is detected, the Arduino sends a signal to the servo motor to close the protective cover.

Testing Using Simulation

The circuit and code were tested using an Arduino simulation platform. The simulation showed that the cover closes when rain is detected and opens again when weather conditions are suitable for drying.

Week 3 – ADVANCED (03/04/2026)
Adding IoT Functionality

In the advanced stage, the system will be improved by adding the ESP8266 WiFi module. This allows the system to connect to the internet and send notifications to the user when rain is detected.

Improving Sensor Monitoring

Additional sensors such as humidity and sunlight sensors will be used to improve the system’s decision making so that clothes dry more efficiently.

Week 4 – MORE (17/04/2026)
Final Testing

The complete system will be tested to ensure all sensors, motors, and controllers work properly together.

Documentation and Demonstration

All project steps, circuit diagrams, code, and system operation will be documented clearly for project demonstration.

Uploading Final Results

Images of the circuit, prototype system, and demonstration results will be uploaded to the GitHub repository to complete the project documentation.
