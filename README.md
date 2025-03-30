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
