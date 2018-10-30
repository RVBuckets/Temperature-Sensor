# WEEK 1
Chose TMP007 Tmperature sensor and reported to professor

# WEEK2
Proposal Submission
[ProposalContentStudent.xlsx](https://github.com/RVBuckets/Temperature-Sensor/files/2508016/ProposalContentStudent.xlsx)

# WEEK3
Created schedule and documented it on github (Schedule.mpp)

# WEEK4
Designed budget and uploaded on github (budget.xlsx)

# WEEK5
Modified the invoice of purchase 
![sensor invoice](https://user-images.githubusercontent.com/42980862/46378577-0d7e1580-c66a-11e8-8f66-190f43ecae79.jpg)
![rpi 3b invoice](https://user-images.githubusercontent.com/42980862/46378580-0fe06f80-c66a-11e8-9cfe-b128d4c62f2f.PNG)

# WEEK6
STUDY DAYS

# WEEK7
Psuedo Assignment due!

# WEEK8
Worked on breadboarding and soldering. Tested my addrress on RPi and noticed my default address as 0x40. Later I realised it should suppose to show 0x47. Worked on pinouts where I connected AD1 to +ve supply and AD0 to SCL and I was able to change my address from 0x40 to 0x47

Steps for pinout (Only for sensor that I'm currently holding):
1) Solder your sensor
2) Follow the RPI Header reference for your pinout to breadboard 
3) Look for the 3V/5V pin from your Rpi and connect it to breadboard (pin no.1)
4) Connect VCC to 3V power supply and GND to common ground (pin no.5 in 2nd Row)
5) Now connect your SCL to I2C clock SCL pin on your RPi(pin no.3 in 2nd Row)
6) Connect SDA to I2C clock SDA pin on your RPI (which is pin no.2 in 2nd Row)


![bboard1](https://user-images.githubusercontent.com/42980862/47366591-0451f880-d6ac-11e8-9067-e740c0f581fb.PNG)
![bboard2](https://user-images.githubusercontent.com/42980862/47366599-074ce900-d6ac-11e8-8676-103b052c9223.PNG)

# WEEK9

Created pcb design as well as schema and exported generated Gerber file to Prototype lab

![schematic](https://user-images.githubusercontent.com/42980862/47753396-c5084680-dc6d-11e8-9605-e20ed6f39082.PNG)
![pcb](https://user-images.githubusercontent.com/42980862/47753398-c8033700-dc6d-11e8-9144-2cbe62a0a0d7.PNG)
