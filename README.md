# Introduction
This project presents the architecture of a low-cost smart vault security and monitoring system. With the help of accessible sensors like Bluetooth modules and IR arrays, as well as inexpensive Arduino UNO microcontrollers for use as a communication channel between the devices, an Internet of Things (IoT)-based security vault system that enables users to monitor and safely store important items and documents for use in homes and businesses has been developed. This system presents a potential zero user interface (UI) touchless technical solution utilizing infrared signals and light-dependent resistance.

# System Design
Initially when the power is turned on the vault as well as its keypad will default to being locked. The first layer of security requires password through Bluetooth connection to access the secondary security system. The Bluetooth module will switch on and start looking for a nearby mobile device to pair with. To pair with the Bluetooth module the user needs to enter the pairing password. Two LEDs (green and red) are used to identify if the provided password is correct or not. Wrong password will activate a buzzer to alert surrounding people. Secondary layer is a keypad designed with IR Sensor-Array which requires ‘secret gesture pattern’ to access the door of the vault. Once the ‘secret gesture pattern’ is entered the user needs to press the LDR switch to confirm. Again, if the wrong password is entered from the keypad the alarm will go off along with the red led indicator. In addition, this system can count transactions of items inside the vault as a third layer security. In this mode, the LED indicators will count if an object is removed or kept inside the vault. If an object is kept inside, green LED will blink once and if an object is removed, the red LED will blink.

## Architecture

![System Functionality](https://github.com/user-attachments/assets/76c23ca0-8301-4e2f-b03e-ca3f6b3ce75b)

## Primary Components
-	Arduino UNO
-	Servo Motors
-	IR sensor-array
-	Bluetooth Module
-	Sonar Sensor
-	Buzzer
-	LDR

## Schematic diagram of the circuit
!Diagrams/Circuit.png

## Prototype Wiring
![image](https://github.com/user-attachments/assets/5b5d8c73-4b88-4ae2-a27d-7592b9817886)

## Security Protocol
- ***First Layer:*** In this state the user needs to input a password via Bluetooth.
- ***Second Layer:*** In this state the user needs to input a gesture pattern on IR sensor array.
- ***Third Layer:*** In this state the object entering or exiting can be identified from the LED indicators.

## Prototype Demonstration

<p align="center"> First Protocol for wrong password  </p>
![1](https://github.com/user-attachments/assets/a5a742ce-0c25-4b04-b28e-4087193e5c2f)


<p align="center"> First Protocol for right password </p>
![image](https://github.com/user-attachments/assets/69176c67-4060-4e64-8971-56bcdeb835a2)

<p align="center"> Second Protocol for wrong password. </p>
![image](https://github.com/user-attachments/assets/df899c14-538b-4433-b436-d5697abd9885)

<p align="center"> Second Protocol for right password. </p>
![image](https://github.com/user-attachments/assets/909d4294-6079-4720-84f8-4aef6b0b3d13) <br>
![image](https://github.com/user-attachments/assets/485cf18f-ca42-4068-af03-e76bdfd56ac3)

<p align="center"> Transaction for entry and removal respectively. </p>
![image](https://github.com/user-attachments/assets/a164a4ff-170a-4816-a933-642d5b40dd52)<br>
![image](https://github.com/user-attachments/assets/e26026dc-4caa-489f-b97b-c87b50be1554)<br>

<p align="center"> Closing of the door. </p>
![image](https://github.com/user-attachments/assets/58980112-4de7-4293-a10c-88113928a93c)
