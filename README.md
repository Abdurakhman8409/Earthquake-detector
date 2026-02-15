# Earthquake Detector System — Arduino + MPU6050

## Overview
Earthquake Detector System is a low‑cost hardware prototype that detects abnormal vibration using an MPU6050 accelerometer and Arduino.  
When strong vibration is detected, the system triggers an alert with LED and buzzer.

## Category
Infomatrix — Hardware Control

## Team
- Bakhtybai Abdurakhman (Grade 9)
- Turarbek Beknur (Grade 9)
- Shakizinda Abdurahim (Grade 9)

Supervisor: Shaizhan Aslan  
School: IT-Lyceum Internat, Taraz

## Goal
To design and test a compact vibration detection and early alert prototype using a microcontroller and motion sensor.

## Hardware Components
- Arduino UNO
- MPU6050 (GY-521)
- LED + 220Ω resistor
- Buzzer
- Breadboard
- Jumper wires

## Wiring

### MPU6050 → Arduino UNO
- VCC → 5V
- GND → GND
- SDA → A4
- SCL → A5

### LED
- D7 → 220Ω → LED(+)
- LED(-) → GND

### Buzzer
- (+) → D8
- (−) → GND

## Detection Algorithm
1. Sensor is initialized and calibrated at startup  
2. Baseline vibration level is measured  
3. Acceleration magnitude is read continuously  
4. Difference from baseline is calculated  
5. If vibration exceeds threshold → ALERT  
6. LED and buzzer are activated

## How to Run
1. Open Arduino IDE  
2. Open `earthquake_detector.ino`  
3. Select Board: Arduino UNO  
4. Select Port (COM)  
5. Upload code  
6. Open Serial Monitor (9600)  
7. Keep device still during calibration  
8. Tap or shake to test detection

## Threshold Tuning
If false alarms occur — increase threshold value in code.  
Typical range: 4000–8000.

## Demo Video
YouTube: https://www.youtube.com/watch?v=2EgKxHBRqJ0

## Project Structure

code/ — Arduino source code  
photos/ — prototype images  
circuit/ — wiring diagram  
docs/ — project documentation  
video/ — demo link
