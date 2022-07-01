---
title: Root Controller ISO About
description: Controller About
published: true
date: 2022-03-18T14:52:57.756Z
tags: cnc controller, root controller, motion controller, isolation
editor: markdown
dateCreated: 2022-02-25T22:12:57.077Z
---

# About
At its core the Root controller is a ESP32 GRBL isolated motion controller (FluidNC). What makes this controller different is the focus of providing **isolated IO** to the **CNC controller**. The controller is designed to accommodate a wide range of operating conditions and machines, to provide ultimate flexibility (its not just a Root CNC Controller).

The controller is designed to isolate the key area of the design to mitigate any nuisance issues when operating in an electrically noisy environment. The design isolates the following areas from one another: Steppers driver outputs (achieved by using externally OPTO isolated drivers), USB, Relays, MOSFETs and RS485. Perfectly suited for the larger CNC machines. 

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/20220202_204658.jpg" width="600">
## Purchase
The Root Controller ISO can be purchased on the Root CNC store
[GOTO SHOP](https://rootcnc.com/product-category/electronics/)

### Key features 
1. 6 axis motion control (Axis ganging can be done via software - 18 digital outputs, can be repurposed)
1. Wide input voltage range (9-36V)
1. Wifi or bluetooth support for remote control and job loading
1. SD card
1. 10 isolated inputs (supporting NPN inductive switches and Standard NC/NO switches)
1. 3 isolated Relay outputs for switching high voltage outputs, say a compressor
1. 3 isolated MOSFET, perfect for driving solenoids for coolant or mist
1. Dedicated Laser output port. 
1. Isolated USB
1. Isolated RS485 (Modbus serial port)

## Demo Video
> Click Image to load youtube video
{.is-info}

 <iframe width="560" height="315"
src="http://www.youtube.com/watch?v=vrsv_Eusyqc" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

[![Demo Video](http://img.youtube.com/vi/vrsv_Eusyqc/0.jpg)](http://www.youtube.com/watch?v=vrsv_Eusyqc "Video Title")


