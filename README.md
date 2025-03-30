# Smart-Garage-Door
### Smart Garage Door IoT Project.
## 💻 Technologies and Tools Used:
### 
💠 Raspberry Pi
###
💠Limit switches (Configured as an input with pull-up resistor)
###
💠Rotary Encoder (Configured as an input with pull-up resistor)
### 
💠Stepper motor
### 
💠EEPROM
### 
💠I2C protocol
### 
💠LED
### 
💠Buttons
## 💡 Key Features of the Device:
###  
💠 The door can be calibrated and opened/closed using buttons.
###  
💠 The door can be stopped while opened/closed by pressing the same button again.
###  
💠 The device remembers its state even if the power goes off.
### 
💠 After powering back on, it waits for a button press and continues from where it stopped. 
### 
💠 If power is lost during calibration, open/close it indicates an error using LEDs, and then the device needs to recalibrate. 
### 
💠 If the door gets stuck, it immediately stops and indicates an error. 
## How the device works: 
The software operates in a state machine consisting of two states. Case 1 is responsible for calibration, and Case 2 is responsible for door open/close operations. When the device powers on, it checks the EEPROM states, and based on the EEPROM states, it directs the system to the relevant case. In each case, a stuck detection is performed, and if the door gets stuck, it immediately stops and recalibrates the door.

The stuck detection is implemented using both interrupt and time-checking methods. Each time the encoder detent is detected, a value is added to the queue. The difference between the two values of the queue(interrupts) is continuously checked, and if it exceeds the tested time, a stuck condition is detected. 

The stopping event during opening and closing is detected by the second interrupt. If a button interrupt is triggered, the button press flag is set to true. The direction is then toggled, and the system runs in the opposite direction if the button is pressed again. 

The system monitors the door and button status, recalibrating if stuck. It toggles the door direction based on button press and uses interrupts for real-time direction and response. 

## Flow chart
###
![Image](https://github.com/user-attachments/assets/719b9521-ea6b-4a63-9827-bc75a2a59f54)
![Image](https://github.com/user-attachments/assets/071edc3e-5278-496d-90f5-a0791349fb6d)

## Demonstration
Watch the demo video here!
###
https://www.linkedin.com/posts/markferdo_iot-embeddedsystems-raspberrypi-activity-7306929983950655488-v2eo?utm_source=share&utm_medium=member_desktop&rcm=ACoAACsg-gEBO2P3dZFz2KSe_CRKzZlLPPhwfDw


