---
title: Outputs
description: Root Controller ISO Outputs
published: true
date: 2022-03-18T16:33:14.847Z
tags: root controller
editor: markdown
dateCreated: 2022-03-18T16:32:01.131Z
---

# Outputs
Aside from the digital outputs of the stepper driver port (Please see [Controller-Stepper](/Controller-Stepper) for more information). The Root Controller has the additional outputs:

- 3x MOSFET output, great for turning lights or solenoids  on/off
- 3x High power relays output, perfectly suited for turning shop vacs on or dust extractors
- Laser/ spindle port, perfect for controlling a PWM device

## MOSFETS
The Root controller has three high power MOSFETs which can be used to switch the power to a number of device, such as solenoids, lights and DC motors. 

The power supply is fed by its dedicated power connector. The input power is internally fused for added protection. The supply can be separate or tied to other supplies depending on your configuration.

The MOSFET area is perfectly suited for switching inductive loads such a solenoids or relays. 

MOSFET control
- FET_1 - on/off control
- FET_2 - on/off control 
- FET_3 - on/off control

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/mosfetoutput.png" width="600">
> Please note depending on the software configuration, not all MOSFET or RELAY output can be used at the same time.
{.is-info}


## Relay output 
The Root controller has three relays outputs which can be used to switch high power loads, such as dust extractors, fume extractors and vacum cleaners. 

These relays are capable of switching mains power with a current of mmmm.

Relay control
- R_1 - on/off control
- R_2 - on/off control 
- R_3 - on/off control

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/relayoutput.png" width="600">
> Please note depending on the software configuration, not all MOSFET or RELAY output can be used at the same time.
{.is-info}

## PWM laser/ Spindle output
The Root controller has a discrete output port which can be used to control a number of different devices. For example: lasers, and discrete control spindles.

Laser/ Spindle control
- EN - on/off control
- DIR - on/off control 
- PWM - on/off control & PWM Control
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/laserport.png" width="600">

> For spindle control, it is advised you use a MODBUS/ RS485 VFD and communicated through the isolated spindle interface.
{.is-info}

> This port is NOT isolated so careful consideration is needed when connecting external devices to ensure the isolation zones are not violated
{.is-warning}
