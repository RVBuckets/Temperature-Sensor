                                                     Temperature-Sensor
                                                      
                                                      
 [Intro](#Introduction)
 [Invoice of Materials](#Invoice of Materials)
 [Time Commitment](#Time Commitment)
 [Parts Assembly](#Parts Assembly)
 [PCB Soldering](#PCB Soldering)
 [Power Up](#Power Up)


# Introduction

### Tmp007 Temperature Sensor

  ![tmp007](https://user-images.githubusercontent.com/42980862/49775866-ae6ef980-fcc7-11e8-9eb0-d16f089b680a.jpg)


Tmp007 breakout has a IR sensor which has a capability of measuring temperature of an object without touching it. This thermopile sensor has an internal math engine which does the calculations of temperature. This embedded thermopile generates micro voltage which is a key for calculating temperature.This sensor is useful to calculate average temperature of surroundings. This sensor works with 2.5V to 5V which does not require any logic shifting.


### Raspberry Pi 3b+

![rpi3b](https://user-images.githubusercontent.com/42980862/49776194-078b5d00-fcc9-11e8-8d61-f96a17dfd31c.PNG)



Also known as Rpi 3b+ is the newest as well as fastest pocket sized computer. 

### Features and Specifications:

- 1.4GHz 64-bit quad-core processor
- dual-band wireless LAN
- Bluetooth 4.2/BLE
- Faster Ethernet
- Power-over-Ethernet support 
- 4 USB 2.0 ports
- 5V/2.5A DC power input
- MicroSD for setting up Operating System as well as storing personal data






                                                    System Diagram

![systemdiagram](https://user-images.githubusercontent.com/42980862/49775550-8cc14280-fcc6-11e8-82c5-ffb05ed6f063.PNG)

System Diagram explains communication of sensor with Raspberry Pi and demonstrates its functioning with Real-Time process.

### Steps for setting up Rpi:

a. Setup SD card:

  - **NOOBS** is the recommended as well as easy to install software for initializing Raspberry Pi. 
  - Insert SD card underneath Rpi's micro SD card slot
 
b. Connections:

   - HDMI cable,Ethernet cable,Keyboard,mouse 
   
  **Note** - Switch computer display to HDMI from VGA to initialize raspberry PI
           - Must see red led on rpi and blinking green led. 
           - During the setup, system will ask user to set username,password
      
 c. Setting up files for internet connection:
 
  - Issue the following command: ``` sudo /etc/network/interfaces``` to make changes in wpa_supplicant.conf which looks like:
  
  ```
  network={
	ssid="myWi-Fi@Humber"
	key_mgmt=WPA-EAP
	auth_alg=OPEN
	eap=PEAP
	identity="Username or N-Number"
	password="Password"
	phase1="peaplabel=0"
	phase2="auth=MSCHAPV2"
	priority=999
	proactive_key_caching=1
}
```
**Make sure to reboot!**

   - In order to run program from Putty, turn on ```SSH``` options from ```Interface``` option from Rpi
   - For Sensor readings, enable ```GPIO feature```
              
 
 
 Startup Screen looks like:
 
  
   ![startscreen](https://user-images.githubusercontent.com/42980862/49777295-f1cc6680-fccd-11e8-8aad-ea40f830cb08.PNG)
   
  
  Fresh Screen after setup:
  
![pi-desktop](https://user-images.githubusercontent.com/42980862/49777538-e62d6f80-fcce-11e8-9446-ed2d50d9548e.png)


### In order to get rid of using HDMI, mouse and a keyboard there's an alternative steps:

- Before making any connection to Rpi make sure to perform te steps

    a. Go to ```Network And Sharing Center``` option from control panel and go to your actual Wifi connection to which computer is connected to and then go to ```properties/Sharing``` which looks like:
    
    ![wifi stat](https://user-images.githubusercontent.com/42980862/49777786-f1cd6600-fccf-11e8-9720-2d31cc633486.PNG)
    
    b. Enable the following option:  
    - [x] Allow other network users to connect through this computer's internet connection. 
    And in the dropdown list choose your Ethernet option
    
    ![ethrnt](https://user-images.githubusercontent.com/42980862/49778059-445b5200-fcd1-11e8-9e32-a4653de4528f.PNG)
    
    This will assign IP address to your raspberry Pi.
    
    c. Go to remote desktop connection and go for ```raspberrypi.mashome.net```
    
    ![image](https://user-images.githubusercontent.com/42980862/49778147-ab790680-fcd1-11e8-9469-78ef9798cf00.png)
    
    


    






# Invoice of Materials

### Materias required:

1. Raspberry Pi 3b+
2. USB to ethernet Connector (Owned)
3. Tmp007 Sensor 
4. Wire Cutter, Pliers, Safety Glass, Jumper Wire, Breadboard

Summary of items purchased

| Item Name | Purchased From | Items in number | Item Price (All price including tax and shipping) | 
|  --- | --- | --- | --- |
| Raspberry Pi 3b+ | SparkFun | 1 | $89.95 |
| Tmp007 Sensor (old/Damaged) | Adafruit | 1 | $36.14 |
| Tmp007 Sensor (New) | Adafruit | 1 | $42.57 |

Total Cost of hardware bought : $ 168.66

For more details on budget: 
[Budget](https://github.com/RVBuckets/Temperature-Sensor/blob/master/Budget.xlsx)


# Time Commitment



![image](https://user-images.githubusercontent.com/42980862/49388670-74fc2400-f6f2-11e8-93a5-1b9dcac88cc5.png)


# Mechanical Assembly

As per adafruit documentation,Tmp007 sensor comes with 0x40 address. This address can be changed to 0x47 by:


Steps for pinout:

1) Soldering the sensor  (**NOT WITHOUT SAFETY GLASS**)


![solder](https://user-images.githubusercontent.com/42980862/49779644-22fe6400-fcd9-11e8-8ebf-55a8b3474cec.PNG)


2) Follow the RPI Header reference for your pinout to breadboard 



![gpio](https://user-images.githubusercontent.com/42980862/49779833-f565ea80-fcd9-11e8-99f3-79126350f276.PNG)



3) 3V power pin from your Rpi and connect it to breadboard ( pin no.1)

4) Connect VCC to 3V power supply and GND to common ground ( pin no.9 )

5) Connect SCL to I2C clock SCL pin on your RPi( pin no.5 )

6) Connect SDA to I2C clock SDA pin on your RPI ( pin no.3 )

7) Now connect AD0 --> SCL and AD1 --> Vcc

![bboard2](https://user-images.githubusercontent.com/42980862/47366599-074ce900-d6ac-11e8-8676-103b052c9223.PNG)
 
8) For detecting the target address of sensor on rpi could be performed by issuing  ``` sudo i2cdetect -y 1``` 

![address0x47](https://user-images.githubusercontent.com/42980862/49780421-74f4b900-fcdc-11e8-8123-e50d4078f324.PNG)

# PCB/Soldering

[Fritizing application](http://fritzing.org/download/) is a very useful tool for composing the PCB which later generates Gerber File that has 9 listing files with top as well bottom dimensions of PCB. 

![pcb](https://user-images.githubusercontent.com/42980862/49780661-84c0cd00-fcdd-11e8-9e5e-e9e8104e7acf.PNG)

For further construction of PCB, **a 5 pin header for required for Rpi and a 8 pin header is required for mounting Sensor.**
 
### 5 Steps for Soldering:
1. Heat up your iron (600-700 degrees F or 315-370 degrees C)

![a](https://user-images.githubusercontent.com/42980862/49781457-cb63f680-fce0-11e8-82eb-613669997e40.PNG)

2. Make sure connection are mechanically stable using helping hands to keep parts steady.

![b](https://user-images.githubusercontent.com/42980862/49781552-2b5a9d00-fce1-11e8-82dd-deca47e9e57e.PNG)

3. Clean iron that builds oxide layer, which inhibits heat transfer and solder adhesion using sponge wire.

![image](https://user-images.githubusercontent.com/42980862/49781575-43cab780-fce1-11e8-95ad-500c5b4705eb.png)

4. Apply heat and solder (soldering time sometimes varies)

![c](https://user-images.githubusercontent.com/42980862/49781732-dd926480-fce1-11e8-9c6f-daf2468aa2b8.PNG)

5. Inspect the join ( Smooth and shiny surface can be observed using a microscope)

### Following is my PCB soldered 

![48098635-5e45d880-e1eb-11e8-857f-df232c8649d1](https://user-images.githubusercontent.com/42980862/49781944-850f9700-fce2-11e8-80d7-34072f034570.JPG)


# Power Up

So far system was able to detect the revised address different from default address. The main purpose of Power up is to display readings just like a product ready for functioning. At this time, my sensor should able to detect the surrounding temperature explaining the real concept of real-time process. 

Following is the program listing of my sensor which s written in python.

```
import smbus
import time

# Get I2C bus
bus = smbus.SMBus(1)

# TMP007 address, 0x40(64)
# Select configuration register, 0x02(02)
#		0x1540(5440)	Continuous Conversion mode, Comparator mode
data = [0x1540]
bus.write_i2c_block_data(0x47, 0x02, data)

time.sleep(0.5)

# TMP007 address, 0x40(64)
# Read data back from 0x03(03), 2 bytes
# cTemp MSB, cTemp LSB
data = bus.read_i2c_block_data(0x47, 0x03, 2)

# Convert the data to 14-bits
cTemp = ((data[0] * 256 + (data[1] & 0xFC)) / 4)
if cTemp > 8191 :
	cTemp -= 16384
cTemp = cTemp * 0.03125
fTemp = cTemp * 1.8 + 32

# Output data to screen
print "Object Temperature in Celsius : %.2f C" %cTemp
print "Object Temperature in Fahrenheit : %.2f F" %fTemp

```
### Understanding the Program Listing

# Unit Testing

To run the following code on rpi, issue the following command ``` sudo python Tmp007.py ```

![readings](https://user-images.githubusercontent.com/42980862/49782514-a1143800-fce4-11e8-83d5-db8f6a728b36.PNG)








