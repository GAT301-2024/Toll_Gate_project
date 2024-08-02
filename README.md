# Toll_Gate_project

**OKOT_SUNDAY_MARK_23-U-2250-GIM-PS**

Ultrasonic Sensor and Servo Motor Control
This Arduino sketch demonstrates how to use an ultrasonic sensor to measure distance and control a servo motor based on the measured distance.

**Components Required**
Arduino board (e.g., Arduino Uno)
Ultrasonic sensor (e.g., HC-SR04)
Servo motor
Jumper wires
Breadboard and power supply

**Circuit Connections**
Ultrasonic sensor Trig pin to Arduino digital pin 6
Ultrasonic sensor Echo pin to Arduino digital pin 7
Servo motor signal pin to Arduino digital pin 9
Servo motor power and ground to appropriate power supply (ensure correct voltage and current rating)
Ultrasonic sensor VCC and GND to Arduino 5V and GND, respectively

**Libraries Used**
Servo.h: To control the servo motor.

**Code Overview**
Global Variables
**Servo myservo;**: Creates a servo object to control the servo motor.
int pos = 0;: Variable to store the position of the servo motor.
int cm = 0;: Variable to store the distance measured by the ultrasonic sensor in centimeters.
**Function**: readUltrasonicDistance

**Parameters**: triggerPin, echoPin

**Returns**: Distance measured by the ultrasonic sensor in microseconds.

**Description**: Sends a pulse to the ultrasonic sensor and measures the time it takes for the echo to return.

**Function**: setup
Initializes the serial communication at 9600 baud rate.
Attaches the servo motor to pin 9.
Sets digital pin 12 to LOW (not used in this sketch but included for potential future use).

**Function:** loop
Measures the distance using the ultrasonic sensor.
If the measured distance is less than 30 cm, it prints the distance to the serial monitor.
Moves the servo motor from 0 to 120 degrees and back to 0 degrees with a delay between steps.

**How to Use**
Connect the components as described in the "Circuit Connections" section.
Upload the code to your Arduino board using the Arduino IDE.
Open the Serial Monitor in the Arduino IDE to view the distance measurements.
Place an object within 30 cm of the ultrasonic sensor to see the servo motor in action.

**Notes**
Ensure that the servo motor and ultrasonic sensor are properly powered.
The servo motor will only move if the measured distance is less than 30 cm.
Adjust the triggerPin and echoPin variables if you connect the ultrasonic sensor to different pins.
