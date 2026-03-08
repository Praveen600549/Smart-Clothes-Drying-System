# Motion Sensor Light Using Arduino

## Project Title

Smart Motion Sensor Light for Home Automation

## Description

This project demonstrates a simple home automation system using an Arduino microcontroller and a PIR motion sensor. The system automatically turns on a light when motion is detected and turns it off when no motion is present.

The purpose of this project is to create a basic robotic system that helps with daily household tasks, such as automatically controlling lights to improve convenience and save electricity.

This system can be used in places like hallways, bathrooms, garages, and staircases where lights are only needed when someone is present.

## Components

* Arduino Uno
* PIR Motion Sensor (HC-SR501)
* LED
* 220Ω Resistor
* Breadboard
* Jumper wires
* USB cable

## Circuit Diagram

Connections used in the project:

PIR Sensor:

* VCC → Arduino 5V
* GND → Arduino GND
* OUT → Arduino Pin 2

LED:

* Long leg (Anode) → Arduino Pin 13
* Short leg (Cathode) → Resistor → GND

## Code

```cpp
int pirPin = 2;
int ledPin = 13;

void setup() {
  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  int motion = digitalRead(pirPin);

  if (motion == HIGH) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }
}
```

## Weekly Updates

### Week 1 – INTRO (06/03/2026)

* Selected project topic: Motion Sensor Light
* Explained project idea and objectives
* Listed components required for the project

### Week 2 – BASICS (20/03/2026)

* Built the basic circuit using Arduino and PIR sensor
* Implemented the Arduino code
* Tested the system using Wokwi simulation

### Week 3 – ADVANCED (03/04/2026)

* Improve system by adding a relay module to control a real light bulb
* Optimize sensor sensitivity and delay settings

### Week 4 – MORE (17/04/2026)

* Final testing of the project
* Documentation and demonstration
* Upload final results and images to GitHub repository
