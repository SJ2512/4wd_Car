# Components
## 4wd chasis platform
## Arduino UNO
## SG90 servo
## Ultrasonic Sensor with its holder 
## 4 BO motors 
## 3S Lithium Ion battery 
## L298N Motor Drivers

## the connections were simple enough and the ultrasonic was mounted on the top of the servo and a threshold of some 20-25 cm was set 
## when the ultrasonic detects an obstacle close enough within the threshold range the arduino stops the motors via motor driver and then the ultrasonic rotates left and right with the help of servo to check for the obstacle free path and then arduino turns in the direction suitable
## here no buck converted is used because i powered the arduino directly from the L298N 5v pin 
