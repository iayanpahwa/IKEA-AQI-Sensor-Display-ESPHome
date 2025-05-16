# IKEA-AQI-Sensor-Display-ESPHome

![logo](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/6.JPG)

Ikea makes a great PM2.5 sensor called VINDRIKTNING, but :
    - It doesn't have a display to show value of PM2.5
    - It's not internet enabled so not much you can do with it 

So let's hack it using ESP8266, make it home-assistant capable using ESPHome and also add a small OLED Display (SSD1306) to see the value of PM2.5 right on the device itself.
------

Requirements :

1. Ikea VINDRIKTNING 
2. Home-Assistant Setup
3. ESPHome 
4. ESP8266 (I used D1-Mini board, it fits well)
5. SSD1306 OLED Display, I used 128x32 pixels
6. Soldering station & wires


Step 1: Open the VINDRIKTNING and locate 5v, Gnd and RST pad on the main board 

![1](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/1.jpeg)


Step 2: Connect 5v to Vin, Gnd to Gnd and RST to Pin D7

![2](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/2.JPG)


Step 3 : Connect Vcc on Oled display to 5v or 3.3v, Gnd to Gnd, SDA to D1 and SCL to D2

![3](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/3.JPG)


Step 4: Use the ESPHome configuration available in file AQI-Monitor.yaml 

![4](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/4.JPG)


Benchmarked with my Xiaomi air purifier sensor reading : 

![5](https://github.com/iayanpahwa/IKEA-AQI-Sensor-Display-ESPHome/blob/main/img/5.JPG)
