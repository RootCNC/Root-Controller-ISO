---
title: Stepper Output
description: How to connect a stepper motor drivers
published: true
date: 2022-03-14T22:03:30.580Z
tags: root controller
editor: markdown
dateCreated: 2022-03-14T21:25:24.539Z
---

# Stepper control
The Root Controller is specifically designed to control OPTO isolated external stepper motor drivers. The reason for this is due to their high current demands of their logic inputs on the motor driver, these are typically around 10-20mA per input (enable signals are typically lower as these do tend not to toggle). These sort of current demands normally exceeds the max electronic IC package current. Exceeding these values can impact the life of the electronic products - the Root controller ISO has been designed to take this into account and will happily supply the max current across all its outputs and provide a long life for the electronics.

The Root controller Rev `2.1` and onwards supports both `common Anode` and `common Cathode` external motor drivers, with the use of the `ref set` settings. 

Some drivers might expose both anode and cathode per input, if this is the case then the wiring will need to be configured into either common anode or common cathode. please see example wiring configurations for more information

# Stepper Driver Outputs
The Root controller support six software configurable stepper motor outputs. These are accessable via a 4 port plug.

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/sleeper_output_ports.png" width="600">


When not using these ports for the stepper motor controller, then the remaining ports can be reconfigured in software to support discrete outputs.

# Ref Set 
> The Root Controller has two configurable jumpers to set its reference point for either common anode or cathode, please ensure these are correctly configured. More information below.  {.is-info} 

The Root controller comes in two options at the time of purchase (the expansion port can be purchased at a later date to add extra inputs and output - the Root 3 onwards requires the full Root controller ISO). 
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/refset_port.png" width="600">
Both headers on the Root Controller need to be set correctly in order for correct operation, these are denoted as `ref set` on the controller label. You can mix the top and bottom reference points but you’ll need to ensure the three outputs per layer are set correctly with the corresponding outputs. Its recommended to set the ref set points to same configurations.

- Ref set 1 - sets the reference point for axis outputs X, Y, Z
- Ref set 2 - sets the reference point for axis outputs A, B, C
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/refset_layers.png" width="600">
> Please note these outputs are software configurable. The Root 3 onwards will use either axis outputs of A, B, C to be the second Y (YII) axis. If you are planning on using the root controller for other style of machines; the software supports up to two outputs per axis. For example the MPCNC Which has XII and YII which will use ports A,B.{.is-info} 

> Beta card can accommodate both common anode and common cathode by default{.is-info} 

>` Rev 2.0` only supports a common cathode (0V reference)  {.is-info} 

# Wiring
## 5V reference (Common Anode)
Below is a list of known external motor drivers to work in the common anode configuration. 
* DM320
* DM332
### Example wiring
Here is an example wiring configuration for a common anode setup
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/stepper-motor-anode.png" width="600">

## 0V reference (Common Cathode)
Be,ow is a list of known external motor driver to work in the common cathode arrangement

>  My Root 4 and 4 Lite both use the common cathode setup

* DM542
* DM556
* DM860
### Example Wiring
Here is an example wiring configuration for a common Cathod setup:
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/stepper-motor-cathode.png" width="600">