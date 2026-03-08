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

https://wokwi.com/projects/457921932420225025


## Weekly Updates

## Week 1 – INTRO (06/03/2026)

### Selected Project Topic

The selected project is **Motion Sensor Light using Arduino**. This project focuses on creating a simple home automation system that can automatically turn on a light when motion is detected.

### Project Idea

The idea of the project is to use a **PIR motion sensor** with an **Arduino Uno** to detect human movement. When motion is detected, the Arduino will turn on a light (LED). When there is no motion, the light will turn off automatically. This helps improve convenience and can also save electricity in homes.

### Project Objectives

* To learn the basics of Arduino and sensors
* To build a simple home automation system
* To detect motion using a PIR sensor
* To automatically control a light based on motion detection

### Components Required

* Arduino Uno
* PIR Motion Sensor (HC-SR501)
* LED
* 220Ω Resistor
* Breadboard
* Jumper wires
* USB cable

---

## Week 2 – BASICS (20/03/2026)

### Building the Basic Circuit

The basic circuit was created by connecting the PIR motion sensor and LED to the Arduino Uno using a breadboard. The PIR sensor detects motion and sends a signal to the Arduino.

### Implementing the Arduino Code

The Arduino program was written to read the signal from the PIR sensor. If motion is detected, the Arduino sends a signal to turn the LED on. If no motion is detected, the LED remains off.

### Testing Using Wokwi

The circuit and code were tested using the **Wokwi Arduino simulator**. The simulation showed that the LED turns on when motion is detected and turns off when no motion is present.

---

## Week 3 – ADVANCED (03/04/2026)

### Adding a Relay Module

In the advanced stage, the system will be improved by adding a **relay module**. This will allow the Arduino to control a real household light bulb instead of just an LED.

### Optimizing Sensor Settings

The PIR sensor settings such as **sensitivity and delay time** will be adjusted to improve the accuracy of motion detection and ensure the light stays on for an appropriate amount of time.

---

## Week 4 – MORE (17/04/2026)

### Final Testing

The complete system will be tested to ensure all components work properly together and the motion detection system functions correctly.

### Documentation and Demonstration

All project steps, circuit diagrams, and code will be documented and explained clearly for demonstration purposes.

### Uploading Final Results

Images of the circuit, simulation results, and final project implementation will be uploaded to the **GitHub repository** to complete the project documentation.

