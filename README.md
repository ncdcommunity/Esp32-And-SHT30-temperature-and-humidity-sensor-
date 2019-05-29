# Interfacing-SHT30-with-esp32-
Displaying Temperature Data on Ubidots  using esp32 and SHT30.
![alt tag](https://github.com/mjScientech/Esp32-And-SHT30/blob/master/SHT30_I2CS_A_1_c02a9c53-2431-4fb7-b568-b403fcd5f63f_480x480.png)
# SHT30
SHT30 is the next generation of Sensirion’s temperature and humidity sensors.

The SHT30 has increased intelligence, reliability and improved accuracy specifications compared to its predecessor. Its functionality includes enhanced signal processing,  so that temperature and humidity can be read out using I2C communications.

This I2C Mini Module makes it easy to read termperature and humidity using our standardized sensor footprint. Plug into a Particle interface module for cloud access from anywhere in the world.

![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/ESP32_1.png)
# ESP-32
The ESP32 makes it easy to use the Arduino IDE and the Arduino Wire Language for IoT applications. This ESp32 IoT Module combines Wi-Fi, Bluetooth, and Bluetooth BLE for a variety of diverse applications. This module comes fully-equipped with 2 CPU cores that can be controlled and powered individually, and with an adjustable clock frequency of 80 MHz to 240 MHz. This ESP32 IoT WiFi BLE Module with Integrated USB is designed to fit in all ncd.io IoT products.

Monitor sensors and control relays, FETs, PWM controllers, solenoids, valves, motors and much more from anywhere in the world using a web page or a dedicated server.

We manufactured our own version of the ESP32 to fit into NCD IoT devices, offering more expansion options than any other device in the world! Integrated USB port allows easy programming of the ESP32. The ESP32 IoT WiFi BLE Module is an incredible platform for IoT application development. This ESP32 IoT WiFi BLE Module can be programmed using Arduino IDE.

Hardware needed Interfacing-SI7021-with-esp32:
- [ESP-32](https://store.ncd.io/product/esp32-iot-wifi-ble-module-with-integrated-usb/)
- [SHT30](https://shop.controleverything.com/products/humidity-and-temperature-sensor-3-rh-0-3-c)
- [I2C Cable](https://store.ncd.io/product/i2c-cable/)
- [PARTICLE ELECTRON OR PHOTON COMPATIBLE I2C SHIELD](https://shop.controleverything.com/products/i2c-breakout-for-particle-electron-or-particle-photon)

Software Used:
- Arduino IDE
- [Ubidot](https://ubidots.com/)


# Steps to send data to Ubidot using ESP-32 and SI7021-

## Connection of SHT30 with shield
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/I2Cconnection%20SI021.JPG)

## Connection of ESP-32 with shield
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/Esp32%20Connection.png)

##  Uploading the code  to ESP32 using Arduino IDE:
- Download and install the PubSubClient Library.
- You must assign your unique Ubidots TOKEN, MQTTCLIENTNAME, SSID (WiFi Name) and Password of the available network.
- Compile and upload the  [ESP32_SHT30.](https://github.com/mjScientech/Esp32-And-SHT30/blob/master/ESP32_SHT30.ino) code.
- To verify the connectivity of the device and the data sent, open the serial monitor.If no response is seen, try unplugging your ESP32 and then plugging it again. Make sure the baud rate of the Serial monitor is set to the same one specified in your code 115200.



## Making the Ubidot work:
- Create the account on [Ubidot](https://ubidots.com/).
- Go to my profile and note down the token key which is a unique key for every account and paste it to your ESP32 code before uploading.
- Add a new device to your ubidot dashboard name esp32.
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/Device.JPG)

- Inside device create new variable name sensor in which your temperature reading will be shown.
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/variable.JPG)

# OUTPUT
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/tempoutput.JPG)


