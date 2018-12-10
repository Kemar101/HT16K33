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

# Bill of Materials and Budget
[Adafruit Small 1.2" 8x8 LED Matrix w/I2C Backpack - Red](https://www.adafruit.com/product/1049)
[Keyestudio 8x8 Dot Matrix Module (3PCS)](http://www.keyestudio.com/ks0336.html)
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/led.jpg" width="500" />

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
