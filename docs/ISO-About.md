---
title: About
description: Root Controller ISO About
published: true
date: 2022-03-18T14:52:57.756Z
tags: cnc controller, root controller, motion controller, isolation
editor: markdown
dateCreated: 2022-02-25T22:12:57.077Z
---

# About
At its core the Root controller is a ESP32 GRBL isolated motion controller (FluidNC). What makes this controller different is the focus of providing **isolated IO** to the **CNC controller**. The controller is designed to accommodate a wide range of operating conditions and machines, to provide ultimate flexibility (its not just a Root CNC Controller).

The controller is designed to isolate the key area of the design to mitigate any nuisance issues when operating in an electrically noisy environment. The design isolates the following areas from one another: Steppers driver outputs (achieved by using externally OPTO isolated drivers), USB, Relays, MOSFETs and RS485. Perfectly suited for the larger CNC machines. 

![Root Controller Rev 2.1 ](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/ex_20220321_224956.jpg)

## Key features 
1. **6 axis motion control** (Axis ganging can be done via software - 18 digital outputs, can be repurposed)
2. **Wide input voltage** range (9-36V)
3. **Wifi or bluetooth** support for remote control and job loading
4. **SD card**
5. **10 isolated inputs** (supporting NPN inductive switches and Standard NC/NO switches)
6. **3 isolated Relay** outputs for switching high voltage outputs, say a compressor
7. **3 isolated MOSFET**, perfect for driving solenoids for coolant or mist
8. Dedicated **Laser output port**. 
9. **Isolated USB**
10. **Isolated RS485** (Modbus serial port)

## Demo Video
> Click Image to load youtube video
{.is-info}

 <iframe width="560" height="315"
src="http://www.youtube.com/watch?v=vrsv_Eusyqc" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

[![Demo Video](http://img.youtube.com/vi/vrsv_Eusyqc/0.jpg)](http://www.youtube.com/watch?v=vrsv_Eusyqc "Video Title")
## Purchase
The Root Controller ISO can be purchased on the Root CNC store
[GOTO SHOP](https://rootcnc.com/product-category/electronics/)
## Electrical Specification 
Details can be found [**here**](https://github.com/RootCNC/Root-Controller-ISO/blob/master/docs/ElectricalSpec.md). If you require additional information I have missed, please contact me and I'll get it added.
## Wiring information
For more information on how to wire and connect the Root Controller to external drives, sensors and other peripherals. please see the Wiki site. [Link to the WIKI](https://wiki.rootcnc.com/)
## Software pinouts
To control the hardware the pinout of peripherals needs to be known, the link **[here](https://github.com/RootCNC/Root-Controller-ISO/blob/master/docs/Pinout.md)** is a convenient way to map Input and Output to the software.
## Software Configurations
For basic configurations for your machine, please see the sub folder names "Configurations"
## Mechanical dimensions
![Root Controller Rev 2.0 dimensions](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/Dimensions_Rev2.1.PNG)
## PCB layout
![Root Controller Rev 2.0 PCB Layout](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/IO_Layout.svg)

## What is Root CNC
For Root CNC project information 
visit [the website](https://rootcnc.com)
## Social links

 1. [Facebook Group](https://www.facebook.com/groups/rootcnc/) 
 2. [Discourse](https://rootcnc.discourse.group/) 
 3. [Discord](https://discord.gg/93Ue5SwthW) Great for quick answer to questions and firmware support
 4. [Thingiverse](https://www.thingiverse.com/sailorpete/designs) 
 5. [Youtube](https://www.youtube.com/c/sailorpete12/)

## License

This project is licensed under the Creative Commons 4.0 license with 
Attribution-NonCommerial-ShareAlike see `LICENSE.txt` for details
