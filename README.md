# HT16K33
## Table of Contents
1. [Introduction](#introduction)
2. [Bill of Materials/Budget](#bill-of-Materials-and-Budget)
3. [Time Commitment](#time-Commitment)
4. [Mechanical Assembly](#mechanical-Assembly)
5. [PCB and Soldering](#pCB-and-Soldering)
6. [Power Up](#power-Up)
7. [Unit Testing](#unit-Testing)
8. [Production Testing](#production-Testing)

# Introduction
This is a single interface board on a raspberry pi 3 that is accesed using vnc or hdmi with tv and keyboard. we solder a pcb board so that we avoid the hassle of wireing makeing the project more clean.

# Bill of Materials and Budget
Can buy the [Adafruit Small 1.2" 8x8 LED Matrix w/I2C Backpack - Red](https://www.adafruit.com/product/1049) or the 
[Keyestudio 8x8 Dot Matrix Module (3PCS)](http://www.keyestudio.com/ks0336.html) would recommend the keyestudio because you get 3 for the price of 1 so if you make a mistake you have 2 more
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/led.jpg" width="500" />

[CanaKit Raspberry Pi 3 B+ (B Plus) Starter Kit (32 GB EVO+ Edition, Premium Black Case)](https://www.amazon.com/dp/B07BCC8PK7?aaxitk=VJ0x-KEWwd4MELp4ZjU-PA&pd_rd_i=B07BCC8PK7&pf_rd_p=3ff6092e-8451-438b-8278-7e94064b4d42&hsa_cr_id=2799715720501&sb-ci-n=productDescription&sb-ci-v=CanaKit%20Raspberry%20Pi%203%20B%2B%20(B%20Plus)%20Starter%20Kit%20(32%20GB%20EVO%2B%20Edition%2C%20Premium%20Black%20Case))
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/pie.jpg" width="500" />

| Parts | Price|
| --- | --- |
| LED | $9.99 |
| Pi3| $79.99 |
| Total | $89.98 |


# Time Commitment

# Mechanical Assembly
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/fullc.jpg" width="500" />

# PCB and Soldering
| HT16K33 | Raspberry Pi |
| --- | --- |
| GND | Pin-06 |
| Vcc | Pin-01(3.3V) Can also use Pin 02(5V)|
| SDA | Pin-03(I2C SDA) |
| SCL | Pin-05(I2C SCL) |

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/Capture.JPG" width="500" />
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/sm1.jpg" width="500" />
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/sm2.jpg" width="500" />

# Power Up
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/i2cdetect.JPG" width="500" />

# Unit Testing
Command: sudo apt-get update

Command: sudo apt-get install build-essential python-dev

Command: sudo apt-get install python-smbus

You need the Python Imaging Library (PIL) which adds image processing capabilities to your Python interpreter.

Command: sudo apt-get python-imaging

After executing the four commands above now you have to install the Adafruit Python LED Backpack.

Step 1: Create a folder in your home directory (/pi/home/) with the name “led”.

Step 2: Download the Adafruit Python LED Backpack with the following command.

Command: sudo git clone https://github.com/adafruit/Adafruit_Python_LED_Backpack.git

After successfully downloading the library go into the led folder “/home/pi/led/Adafruit_Python_LED_Backpack” and execute the following command to install the library on your Raspberry Pi

Command: sudo python setup.py install

To execute the Adafruit LED test example go into the folder “/home/pi/led/Adafruit_Python_LED_Backpack/example” and execute the “matrix8x8_test.py” program if the I2C address is correct for your LED matrix.

Command: python matrix8x8_test.py

The program should activate the LED’s and show a X with a frame on the LED matrix at the end.

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/display.jpg" width="500" />

# Production Testing
?
