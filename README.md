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
##1.2″ 4-Digit 7-Segment display

## Database Design
The database connection is established and connected to the mobile application. Reading and writing from the sensor to the database are also required. The database utilizes user-authentication to allow maximum security and protection for the users information. In order to read and write temperature, the user must be registered using a username and password through authentication processing. Offline mode allows access to the app, without the need to register and login. Offline mode skips user-authentication, and moves the user to the actual app. In offline mode, there will be no form of communications to the database.  Therefore the user is unable to read/write temperature to the database. 

## Testing for Hardware
