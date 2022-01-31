<img align="right" width=175 src="https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/R_Logo.png" />

# About
At its core the Root controller is a ESP32 GRBL isolated motion controller (FluidNC). What makes this controller different is the focus of providing **isolated IO** to the **CNC controller**. The controller is designed to accommodate a wide range of operating conditions and machines, to provide ultimate flexibility (its not just a Root CNC Controller).

The controller is designed to isolate the key area of the design to mintage any nuisance issues when operating in a electrically noisy environment. The design isolates the following areas from one another. Steppers driver outputs (achieved by using externally OPTO isolated drivers), USB, Relays, MOSFETs and RS485. Perfectly suited for the larger CNC machines. 
![Root Controller Render ](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/Render_1.JPG)

## Key features 
1. 6 axis motion control (Axis ganging can be done via software - 18 digital outputs, can be repurposed)
2. Wide input voltage range (9-30V)
3. Wifi Support for remote control and job loading
4. SD card
5. 10 Isolated input (supporting NPN inductive switches and Standard NC/NO switches)
6. 3 isolated Relay outputs for switching high voltage outputs, say a compressor
7. 3 isolated MOSFET, perfect for driving solenoids for coolant or mist
8. Dedicated Laser output port. 
9. Isolated USB
10. Isolated RS485 (Modbus serial port)

## Purchase
The Root Controller ISO can be purchased on the Root CNC store
[GOTO SHOP](https://rootcnc.com/product-category/electronics/)
## Electrical Specification 
Details can be found [**here**](https://github.com/RootCNC/Root-Controller-ISO/blob/master/docs/ElectricalSpec.md)
if you require additional information I have missed, please contract me and I'll get it added.
## Software pinouts
To control the hardware the pinout of peripherals needs to be known, the link **[here](https://github.com/RootCNC/Root-Controller-ISO/blob/master/docs/Pinout.md)** is a convenient way to map Input and Output to the software.
## Mechanical dimensions
![enter image description here](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/Dimensions_Rev2.0.PNG)
## PCB layout
![Root Controller Rev 2.0 PCB Layout](https://github.com/RootCNC/Root-Controller-ISO/blob/master/Media/IO_Layout.svg)

## What is Root CNC
For Root CNC project information 
visit [the website](https://rootcnc.com)
## Social links

 1. [Facebook Group](https://www.facebook.com/groups/rootcnc/) 
 2. [Discourse](https://rootcnc.discourse.group/) 
 3. [Discord](https://discord.gg/93Ue5SwthW) Great for quick answer to questions
 4. [Thingiverse](https://www.thingiverse.com/sailorpete/designs) 
 5. [Youtube](https://www.youtube.com/c/sailorpete12/)

## License

This project is licensed under the Creative Commons 4.0 license with 
Attribution-NonCommerial-ShareAlike see `LICENSE.txt` for details