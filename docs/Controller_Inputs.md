---
title: Controller Inputs
description: Root Controller Input Section
published: true
date: 2022-05-29T20:56:11.673Z
tags: root controller
editor: markdown
dateCreated: 2022-03-14T22:22:48.038Z
---

# Inputs
The Root controller ISO has isolated inputs which are referenced to the Vin section of the card. Please take note of the isolation boundaries when connecting up the inputs.

The Controller is designed to support normal volt-free switch; such as mechanical switches, either NC (normally closed) or NO (normally open); And/Or NPN inductive sensors. All inputs are electrically the same. For ease of wiring, all axis limit inputs have the same connector and pin out. 

The inputs which are used for “start”, “hold” and “macro” do have a different connector, so please take note of the difference in wiring. Again easy to wiring, Root CNC offer a easy button/ probe point PCB. These can be purchased from the store or downloaded from GitHub.

All inputs are software configured and can be repurposed.

- x6 axis inputs (one per axis, min and max can be combined onto on input. Please see the end stop section for more information)
- x1 probe point
- x3 user configurable inputs (these are typically used for GRBL or fluidnc control signals such as Start, Hold, Reset and Macros.

In total there are *ten* software configurable inputs which can be used for any function.

## Endstops
As mentioned in the pervious section, the Root controller is designed to accommodate voltage free switches, such as mechanical lever switches or NPN inductive switches.

Each input can have two sensors/ switches connected to it, these are typically used on axis with min and max limit switches.

### Inductive Probe Wiring 
> NPN Inductive Switch sensor ONLY {.is-info}

<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/inductive_probe.png" width="600">
### Inductive Probe Min & Max Wiring 
Image comming soon
### Basic Endstop Wiring
In this basic configuration, either NO (Normally Open) Or NC (Normally Closed) switches can be used
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/micro-switch.png" width="600">
### Endstop wiring Min & Max (NO)
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/micro-switch-no.png" width="600">
### Endstop wiring Min & Max (NC)
<img src="https://raw.githubusercontent.com/RootCNC/Root-Controller-ISO/master/Media/micro-switch-nc.png" width="600">
> Please note - NC switches are not recommend on `Y_lim`. IF YOU INTEND TO FLASH THE ROOT CONTROLLER WHILST BEING INSTALLED IN A SYSTEMS. pulling these pins LOW stops the programming routing. If you do use NC switched: then, please ensure these are disconnected piror to programming. 
{.is-warning}
