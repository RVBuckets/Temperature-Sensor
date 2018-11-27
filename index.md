# Temperature-Sensor

# WEEK 13

Presentation Due!  
[HardwareWeek13.pptx](https://github.com/RVBuckets/Temperature-Sensor/files/2621698/HardwareWeek13.pptx)



# WEEK 12

Case ready!! received on Friday and here is the case outlook:

![thumbnail](https://user-images.githubusercontent.com/42980862/49087350-ba1ce380-f224-11e8-984d-f9a295bf2339.jpg)

![thumbnail 1](https://user-images.githubusercontent.com/42980862/49087395-da4ca280-f224-11e8-8690-fba2ed6fac03.jpg)


Emailed the Corel Draw files to Prototype Lab after 4 attempts where I discovered mismatch of notches that didn't actually fit the gap. In my case, I have to resize my case in terms of 3 parameters: Height,width and length only due to my pcb unwanted expanded areas.Vlad helped me to measure the size using Vernier Caliper and following are my case packages:

![rpi2case](https://user-images.githubusercontent.com/42980862/48820425-d7344c80-ed22-11e8-8041-aa1a9c327e5a.jpg)

![case2](https://user-images.githubusercontent.com/42980862/48820431-dbf90080-ed22-11e8-8c55-28a2d4d13be1.PNG)

Corel file on my GitHub account is by name: Modified case.cdr

# WEEK 11

Tested my Sensor on Sunday for readings where I used iPhone flashlight as well as icebag where I noticed fluctuations in my temperature. On the very next day when I tested my sensor on my rpi again it even failed to show the address. To detect I used DMM for testing my sensor as well as I used my group partners' pcb and rpi which confirmed that my sensor was damaged possibly due to "Disengaing it from rpi before detaching my power supply". I ordered new rpi on Monday and fortunately received on Tuesday (Fedex Standard Overnight) and when I again used my new sensor it works in order.
Reading appears to be like:
Using my iPhone flash light



![hightemp](https://user-images.githubusercontent.com/42980862/48458264-93c26700-e793-11e8-8446-88e88e875470.PNG)



Using icebag




![lowtemp](https://user-images.githubusercontent.com/42980862/48458269-9ae97500-e793-11e8-8890-4621d2979f91.PNG)


And my proof of purchase for new sensor ordered on Monday!



![payment](https://user-images.githubusercontent.com/42980862/48458683-5d85e700-e795-11e8-8cfb-3e4049e84ccb.jpg)


# WEEK 10

Recieved pcb from Prototype lab. While receiving pcb, I noticed that there were only 4 input for sensor instead of 6. In order to testify my files, I even demonstrated my files on online gerber viewer which looked alright (as per VLAD) but for some reason prototype lab computer failed to identify the inputs. Later VLAD punctured 2 more holes on my PCB. 
![bottom](https://user-images.githubusercontent.com/42980862/48098629-59812480-e1eb-11e8-9fab-fc21235708eb.JPG)
![top](https://user-images.githubusercontent.com/42980862/48098635-5e45d880-e1eb-11e8-857f-df232c8649d1.JPG)
![pcb pi](https://user-images.githubusercontent.com/42980862/48098631-5c7c1500-e1eb-11e8-81ec-87bd4f963abf.JPG)

# WEEK9

Created pcb design as well as schema and exported generated Gerber file to Prototype lab

![schematic](https://user-images.githubusercontent.com/42980862/47753396-c5084680-dc6d-11e8-9605-e20ed6f39082.PNG)

![pcb](https://user-images.githubusercontent.com/42980862/47753398-c8033700-dc6d-11e8-9144-2cbe62a0a0d7.PNG)


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


# WEEK7

Psuedo Assignment due!


# WEEK6

STUDY DAYS


# WEEK5

Modified the invoice of purchase 

![sensor invoice](https://user-images.githubusercontent.com/42980862/46378577-0d7e1580-c66a-11e8-8f66-190f43ecae79.jpg)

![rpi 3b invoice](https://user-images.githubusercontent.com/42980862/46378580-0fe06f80-c66a-11e8-9cfe-b128d4c62f2f.PNG)


# WEEK4

Designed budget and uploaded on github [Budget.xlsx](https://github.com/RVBuckets/Temperature-Sensor/files/2532209/Budget.xlsx)


# WEEK3

Created schedule and documented it on github



# WEEK2
Proposal Submission 
[ProposalContentStudent.xlsx](https://github.com/RVBuckets/Temperature-Sensor/files/2532218/ProposalContentStudent.xlsx)



# WEEK 1

Chose TMP007 Tmperature sensor and reported to professor


