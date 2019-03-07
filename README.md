# JnJs Clockwork
## Notification Device

## Table of Contents
1. [Introduction](#introduction)
2. [Time Schedule](#time-schedule)
3. [PCB Design Files](#pcb-design-files)
4. [Assembly for Hardware](#assembly-for-hardware)
5. [PCB Soldering](#pcb-soldering)
6. [Power Up](#power-up)
7. [Testing of Hardware](#testing-of-hardware)

## Introduction
JnJ’s Clockwork is an android based alarm mobile application where users are able to set and customize alarms of their choice for daily use. The user will be able to create multiple alarm profiles along with being able to set timers and stopwatches. When connected to its corresponding hardware component, the app furthers its capabilities by allowing users the ability to read local temperatures via the sensor included. The project is designed to give users ease of access to anything time related in a simple and clean formfactor.

## PCB Design Files

## Assembly for Hardware

## PCB Soldering

## Power Up
### HTU21D-F Temperature/Humidity Sensor
With the code provided in this repository, this test code should get your sensor to read and write temperature/humidity.

Firstly though assuming you installed circuit python, all that is required is to run the command line to install HTU21D libraries.
```
sudo pip3 install adafruit-circuitpython-htu21d
```
You can copy this code and run it.

```import time
import board
import busio
from adafruit_htu21d import HTU21D
 
# Create library object using our Bus I2C port
i2c = busio.I2C(board.SCL, board.SDA)
sensor = HTU21D(i2c)
 
 
while True:
    print("\nTemperature: %0.1f C" % sensor.temperature)
    print("Humidity: %0.1f %%" % sensor.relative_humidity)
    time.sleep(2)
```

Finally all that is needed is to run htu21d_simplestest.py

### 1.2″ 4-Digit 7-Segment display
For this sensor we want to be able to display the current time. With that python and its librarys need to be installed:
```
sudo apt-get update
sudo apt-get install build-essential python-dev
```
You would also need python smbus and python-imaging library:
```
sudo apt-get install python-smbus python-imaging
```

Clone the url onto your pi and move into it:
```
git clone https://github.com/adafruit/Adafruit_Python_LED_Backpack
cd Adafruit_Python_LED_Backpack
```
This is the last library you need to install:
```
sudo python setup.py install
```
Now go into your file named Adafruit_LED_Backpack:
```
cd Adafruit_LED_Backpack
```
There are alot of test codes we can use here, but in case we just need our sensor to display the time:
```
sudo python SevenSegment.py
```

## Database Design
The database connection is established and connected to the mobile application. Reading and writing from the sensor to the database are also required. The database utilizes user-authentication to allow maximum security and protection for the users information. In order to read and write temperature, the user must be registered using a username and password through authentication processing. Offline mode allows access to the app, without the need to register and login. Offline mode skips user-authentication, and moves the user to the actual app. In offline mode, there will be no form of communications to the database.  Therefore the user is unable to read/write temperature to the database. 

## Testing for Hardware
