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
This is a single interface board on a raspberry pi 3 that is accesed using vnc or hdmi with tv and keyboard. Would reccomend the vnc this allow you to access the pi anywhere and on any pc. Here is a [Link for VNC setup](https://www.realvnc.com/en/connect/docs/get-connected.html) to establishing a direct connection over a local network (LAN or VPN). Also [Link for VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) that is needed for the setup. We solder a pcb board so that we avoid the hassle of wireing making the project more clean organize and portable. One software used was [Fritzing](http://fritzing.org/download/)for designing the pcb board. Along with [CorelDRAW](https://www.coreldraw.com/en/free-trials/?sourceid=cdgs2018-xx-ppc_brkws&x-vehicle=ppc_brkws&gclid=EAIaIQobChMIo4-G86WW3wIVCZNpCh32gAfJEAAYASABEgI-zfD_BwE) free 15day trial. This is used for our box case, can also use [autoCAD](https://www.autodesk.ca/en/products/autocad/free-trial) free 30 day trial.

# Bill of Materials and Budget
For the material you can buy the [Adafruit Small 1.2" 8x8 LED Matrix w/I2C Backpack - Red](https://www.adafruit.com/product/1049) or the 
[Keyestudio 8x8 Dot Matrix Module (3PCS)](http://www.keyestudio.com/ks0336.html) would recommend the keyestudio because you get 3 for the price of 1 so if you make a mistake you have 2 more.

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/led.jpg" width="300" />
We also purchase a 
[CanaKit Raspberry Pi 3 B+ (B Plus) Starter Kit (32 GB EVO+ Edition, Premium Black Case)](https://www.amazon.com/dp/B07BCC8PK7?aaxitk=VJ0x-KEWwd4MELp4ZjU-PA&pd_rd_i=B07BCC8PK7&pf_rd_p=3ff6092e-8451-438b-8278-7e94064b4d42&hsa_cr_id=2799715720501&sb-ci-n=productDescription&sb-ci-v=CanaKit%20Raspberry%20Pi%203%20B%2B%20(B%20Plus)%20Starter%20Kit%20(32%20GB%20EVO%2B%20Edition%2C%20Premium%20Black%20Case)

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/pie.jpg" width="300" />
Will also need some header for your sensor and the raspberry pi[Adafruit GPIO Header for Raspberry Pi A+/B+ - 2x20 Female Header [ADA2222]](https://www.amazon.com/Adafruit-GPIO-Header-Raspberry-Pi/dp/B00XW2NK1Y/ref=sr_1_10?ie=UTF8&qid=1544481444&sr=8-10&keywords=40+pin+header+raspberry+pi) and [header](https://www.amazon.ca/Gikfun-2-54mm-Stackable-Female-Arduino/dp/B0154KMHE2/ref=sr_1_4?ie=UTF8&qid=1544481861&sr=8-4&keywords=6+pin+header) for the HT16K33 sensor.

| Parts | Price|
| --- | --- |
| LED | $9.99 |
| Pi3| $79.99 |
| Pi3 header| $5.73 |
| Sensor header| $7.22 |
| Total | $102.93 |


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
After connecting 
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/spcb.JPG" width="500" />
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
