# HT16K33 LED DISPLAY

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/nocaseled.JPG" width="300" />

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
This is a single interface board LED Display on a raspberry pi 3 that is accesed using vnc or hdmi with tv and keyboard. Would recommend the vnc this allow you to access the pi anywhere and on any pc. Here is a [Link for VNC setup](https://www.realvnc.com/en/connect/docs/get-connected.html) to establishing a direct connection over a local network (LAN or VPN). Also [Link for VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) that is needed for the setup. We solder a pcb board so that we avoid the hassle of wireing making the project more clean organize and portable. One software used was [Fritzing](http://fritzing.org/download/)for designing the pcb board. Along with [CorelDRAW](https://www.coreldraw.com/en/free-trials/?sourceid=cdgs2018-xx-ppc_brkws&x-vehicle=ppc_brkws&gclid=EAIaIQobChMIo4-G86WW3wIVCZNpCh32gAfJEAAYASABEgI-zfD_BwE) free 15day trial. This is used for our box case, can also use [autoCAD](https://www.autodesk.ca/en/products/autocad/free-trial) free 30 day trial. You will also need and operating system for the raspberry pi download [here](https://www.raspberrypi.org/downloads/raspbian/). To extract the image for the pi a recommended software is [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/). Attach[here](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) is the Installing operating system images guide for installing on a sd card.

# Bill of Materials and Budget
For the material you can buy the [Adafruit Small 1.2" 8x8 LED Matrix w/I2C Backpack - Red](https://www.adafruit.com/product/1049) or the 
[Keyestudio 8x8 Dot Matrix Module (3PCS)](http://www.keyestudio.com/ks0336.html) would recommend the keyestudio because you get 3 for the price of 1 so if you make a mistake you have 2 more.

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/led.jpg" width="300" />

We also purchase a 
[CanaKit Raspberry Pi 3 B+ Starter Kit with 32GB Micro SD Cards and Premium Black Case](https://www.amazon.com/CanaKit-Raspberry-Starter-Premium-Black/dp/B07BCC8PK7/ref=sr_1_1?s=pc&ie=UTF8&qid=1544482698&sr=1-1) this came with a sd card that we use to add the os.

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/pie.jpg" width="300" />

Will also need some header for your sensor and the raspberry pi[Adafruit GPIO Header for Raspberry Pi A+/B+ - 2x20 Female Header [ADA2222]](https://www.amazon.com/Adafruit-GPIO-Header-Raspberry-Pi/dp/B00XW2NK1Y/ref=sr_1_10?ie=UTF8&qid=1544481444&sr=8-10&keywords=40+pin+header+raspberry+pi) and [header](https://www.amazon.ca/Gikfun-2-54mm-Stackable-Female-Arduino/dp/B0154KMHE2/ref=sr_1_4?ie=UTF8&qid=1544481861&sr=8-4&keywords=6+pin+header) for the HT16K33 sensor.
Another component needed would be clear Acrylic sheet to make the case. [Johnson Industrial](http://www.johnstonplastics.com/toronto/)
is a good place to buy your Acrylic sheets from, they also do cutting.

| Parts | Price|
| --- | --- |
| LED | $11.50 |
| Pi3| $91.99 |
| Pi3 header| $6.58 |
| Sensor header| $8.30 |
| Clear Acrylic 12"x24"| $7.18 |
| Acrylic cutting at a dollar per minute x3| $5.25 |
| Total | $130.79 |

Note these prices doesn't not inculde shipping and handling, the price could increase drastically. If you have amazon prime shipping would be free.

# Time Commitment
The time it would take to recreate this project will vary. Ordering the parts can take days if not weeks. Also finding a store to a buy and cut the acrylic for you along with a store to make the pcb board. Considering you have all the parts needed along with your acrylic case cut and pcb board, this project can be made over a weekend.

# Mechanical Assembly
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/fullc.jpg" width="300" />

Attach [here](https://github.com/Kemar101/HT16K33/blob/master/kemar2.cdr) is a link to the CorelDraw file for the case.
After obtaining the corel file and finding a company to lazer cut assemblying the case is simple. The case on it own snaps into place and can be disassemble and reassemble eazy. The raspberry pi can sit in the case or can be screwed down at the bottom.



# PCB and Soldering
| HT16K33 | Raspberry Pi |
| --- | --- |
| GND | Pin-06 |
| Vcc | Pin-01(3.3V) Can also use Pin 02(5V)|
| SDA | Pin-03(I2C SDA) |
| SCL | Pin-05(I2C SCL) |

Attach [here](https://github.com/Kemar101/HT16K33/blob/master/kemar%20projectyy.fzz) is a link to the fritzing file needed to make the pcb board.

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/Capture.JPG" width="500" />

Once the pcb board is make we would need to solder the headers so that you have a clean connection

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/sm1.jpg" width="300" />
<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/sm2.jpg" width="300" />

Note if you do not have a soldering kit you can find a soldering shop near by. If not you can buy a Soldering kit but that would incease your budget factoring the kits price.

# Power Up
After Setting up the pcb should look something like this

<img src="https://raw.githubusercontent.com/Kemar101/HT16K33/master/spcb.JPG" width="500" />

your going to connect to the pi and run the 
Command sudo i2cdetect -y 1
this shows the raspberry pi detect the address and eveything is working

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
In order to mass produce this project I would try and buy every thing in bulk. For example instead of trying to buy 100 raspberry pi for $100, i can contact the retailer that sell the pi to try and get a discount in bulk. The same thing would apply for the Acrylic Sheet, buying them in bulk or multiple large sheets. This would drastically reduce the price to mass produce, than buying them individually.
