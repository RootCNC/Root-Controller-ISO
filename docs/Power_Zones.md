---
title: Root Controller Isolated Power
description: Power Islands on the root controller
published: true
date: 2022-03-18T15:24:18.219Z
tags: root controller
editor: markdown
dateCreated: 2022-03-18T15:19:39.726Z
---

# Power
The Root controller is segregation into multiple isolation zones to suit the individual needs of the CNC builder. The purpose of these zones is to help isolated areas from interfering with one another. For example the spindle control vs the low noise CNC controller zones. The Root controller is well suited for large CNC machines and plasma cutters.

Carefully consideration should be made when planning the electronics for your CNC machine. As optimal performance is dependent on the type of machine you are building. The information below will aid your design. If you feel information is missing, please send me a message and I’ll clarify and aid you.

The controller has the following major areas of isolation:
1. `V_in ISO` - this is used for all inputs and powering the CNC motion controller.
2. `RS-485 isolation zone` - this provides an isolated RS485 interface to talk to your VFD or other peripherals (more items will be added in the future). This zone is typically powered by the VFD and doesn’t require any additional interfaces or PSUs
3. `MOSFET isolation` - this is a separation isolated zone which comprised of three high power MOSFETs. This is powered from a separate power input and is perfect for controlling device which need power, for example Solenoids, lights etc
4. `Controller reference` - this area is not isolated to the CNC controller. isolation is achieved through the OPTO isolated stepper motor drivers. The laser/ spindle port is also referenced to this area. when using this port, careful consider is required to ensure the other isolation zones are not violated.
5. `Relay zone` - three relay outputs are inherently isolated from everything else and between them self.
6. `USB ISO` - the usb type C connector is isolated from the controller to ensure. This is perfect to ensure your expensive laptop or CNC computer is not directly attached to your machine, this help mitigate fault propagation effecting you machine. 

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/powerscheme.png" width="600">

> To ensure optimal performance and noise immunity - please ensure the current return paths and loops are reduced and power zone references are not connected together. E.g. avoid connecting `0V` to `0V_V` 
{.is-warning}


# Powering the controller
Power is applied through the power in connector in the `Vin ISO` zone. The input requires a supply voltage of anything between 12-36v. 

This power supply is internally fused for added protection.

The minimum PSU capacity should greater then `8 watts` to power the controller.

The voltage applied to the controller through this connector is also applied to the controllers inputs power pins. This is useful when powering external sensors, such as inductive probes. The inputs power pins are fused with the same fuse as the main input power connector. 
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/powerinput.png" width="600">