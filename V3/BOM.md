# Components 
## Ultrasonic sensor was replaced by VL53L0X Time of Flight sensor  
(Faster and more accurate)
## BO motors were replaced by 12V 300 RPM generic DC motors  
## L298N was replaced by BTS7960 motor drivers  
## Arduino Mega  
## ESP32  
## Logic level converter  
## Step-down buck converter for ESP32  
## 4S lithium-ion battery  
## Buck converter  

## A dual microcontroller architecture was used, where the Arduino Mega acted as a slave controller obeying commands sent by the ESP32, which acted as the master controller. Both microcontrollers were connected via a logic level converter.
## This was necessary because the Arduino operates on 5V logic levels, while the ESP32 operates on 3.3V logic levels. The logic level converter ensured proper signal translation and reliable communication between the two microcontrollers.
## Commands sent to the Arduino by the ESP32 were single-character instructions such as A, B, C, etc. Each character was mapped in the Arduino firmware to a specific action.
## Example:  
## A – Stop motors and switch to manual driving mode  
## W – Move forward  
## The buck converters were used to step down the battery voltage to 5V, allowing safe power delivery to both the Arduino Mega and the ESP32.
