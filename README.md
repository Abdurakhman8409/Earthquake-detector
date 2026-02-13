# Earthquake Detector System (Prototype) — Arduino

## Overview
A low-cost vibration alert prototype built with Arduino. The system detects abnormal vibration/sound activity and triggers an alert using OLED + LED + buzzer.

## Category
Infomatrix — Hardware Control

## Team
- Bakhtybai Abdurakhman (Grade 9)
- Turarbek Beknur (Grade 9)
- Shakizinda Abdurahim (Grade 9)
Supervisor: Aslan  
School: IT-Lyceum Internat, Taraz

## Problem & Goal
Earthquakes can occur suddenly. Many small institutions need affordable local warning prototypes.
Goal: build and test a compact alert device with adjustable sensitivity.

## How it works
1) Reads sensor values continuously  
2) Compares to a tuned threshold (and/or digital trigger)  
3) If vibration/noise exceeds the limit → ALERT  
4) OLED shows status, LED lights, buzzer sounds

## Components
- Arduino UNO
- Sound/Vibration sensor module (AO/DO)
- OLED 0.96" I2C (SSD1306)
- LED + 220Ω resistor
- Buzzer
- Breadboard + jumper wires

## Wiring
### OLED (I2C)
- VCC → 5V
- GND → GND
- SDA → A4
- SCL → A5

### Sensor module
- VCC → 5V
- GND → GND
- DO  → D2
- AO  → A0

### LED
- D7 → 220Ω → LED(+) ; LED(-) → GND

### Buzzer
- (+) → D8 ; (-) → GND

## How to run
1) Open `code/earthquake_detector.ino` in Arduino IDE  
2) Install libraries: Adafruit SSD1306 + Adafruit GFX  
3) Select Board: Arduino UNO, select Port (COM)  
4) Upload  
5) Open Serial Monitor (9600) and test by tapping the table  
6) Tune threshold in code if needed

## Demo Video
YouTube: (paste link here)

## Photos & Circuit
- Photos: `photos/`
- Wiring diagram: `circuit/wiring.png`

## Future Improvements
- Add MPU6050 accelerometer for more accurate vibration analysis
- Data logging and wireless notifications
- Better filtering to reduce false triggers
