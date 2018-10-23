Steps for pinout (Only for sensor that I'm currently holding):
1) Solder your sensor
2) Follow the RPI Header reference for your pinout to breadboard 
3) Look for the 3V/5V pin from your Rpi and connect it to breadboard (pin no.1)
4) Connect VCC to 3V power supply and GND to common ground (pin no.5 in 2nd Row)
5) Now connect your SCL to I2C clock SCL pin on your RPi(pin no.3 in 2nd Row)
6) Connect SDA to I2C clock SDA pin on your RPI (which is pin no.2 in 2nd Row)


![bboard1](https://user-images.githubusercontent.com/42980862/47366591-0451f880-d6ac-11e8-9067-e740c0f581fb.PNG)
![bboard2](https://user-images.githubusercontent.com/42980862/47366599-074ce900-d6ac-11e8-8676-103b052c9223.PNG)


