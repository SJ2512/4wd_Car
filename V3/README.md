## in this final version of my car i combined everything from the previous version and also upgraded some of its components and created a car which has dual driving mode 
### mode 1 was self driving mode 
### mode 2 was manual driving mode 

## A dual microcontroller architecture was used, where the Arduino Mega acted as a slave controller obeying commands sent by the ESP32, which acted as the master controller. Both microcontrollers were connected via a logic level converter.
## This was necessary because the Arduino operates on 5V logic levels, while the ESP32 operates on 3.3V logic levels. The logic level converter ensured proper signal translation and reliable communication between the two microcontrollers.
## Commands sent to the Arduino by the ESP32 were single-character instructions such as A, B, C, etc. Each character was mapped in the Arduino firmware to a specific action.
## Example:  
## A – Stop motors and switch to manual driving mode  
## W – Move forward  
## The buck converters were used to step down the battery voltage to 5V, allowing safe power delivery to both the Arduino Mega and the ESP32.
