                                                     Temperature-Sensor
                                                      
                                                      
# Intro
# Invoice of Materials
# Time Commitment
# Parts Assembly
# PCB Soldering
# Power Up


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
  
  ```network={
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
    
    b. Enable the following option:  - [x] Allow other network users to connect through this computer's internet connection. And in the dropdown list choose your Ethernet option
    
    ![ethrnt](https://user-images.githubusercontent.com/42980862/49778059-445b5200-fcd1-11e8-9e32-a4653de4528f.PNG)
    
    This will assign IP address to your raspberry Pi.
    
    c. Go to remote desktop connection and go for ```raspberrypi.mashome.net```
    
    ![image](https://user-images.githubusercontent.com/42980862/49778147-ab790680-fcd1-11e8-9469-78ef9798cf00.png)
    
    


    






# Invoice of Materials

Purchase of raspberry pi 3b+

![image](https://user-images.githubusercontent.com/42980862/49388496-0fa83300-f6f2-11e8-95a2-be37b8899de8.png)


First Sensor


![image](https://user-images.githubusercontent.com/42980862/49388602-45e5b280-f6f2-11e8-828f-662df6308c8c.png)


Second Sensor


![image](https://user-images.githubusercontent.com/42980862/49388571-35cdd300-f6f2-11e8-9137-047c14d6517d.png)


# Time Commitment



![image](https://user-images.githubusercontent.com/42980862/49388670-74fc2400-f6f2-11e8-93a5-1b9dcac88cc5.png)
 




