---
title: Inverters
description: Configuration and settings for Inverters
published: true
date: 2022-09-13T07:31:14.847Z
tags: root controller
editor: markdown
dateCreated: 2022-09-13T07:31:14.847Z
---

# Supported Inverters
Supported means they have been tested and verified to work with the RootController by either the RootCNC creator or the community. 
* [Siemens V20](#siemens-v20)

## Siemens Sinamics V20 Inverter<a name="siemens-v20"></a>

[Manual found here](https://cache.industry.siemens.com/dl/files/056/104426056/att_70877/v1/v20_operating_instructions_complete_en-US_en-US.pdf)


These settings are for the [Siemens SINAMICS V20 Converter, 1-Phase In, 550Hz Out, 1.5 kW, 240 V ac, 7.8 A](https://uk.rs-online.com/web/p/inverter-drives/2033539/?relevancy-data=7365617263685F636173636164655F6F726465723D31267365617263685F696E746572666163655F6E616D653D4931384E525353746F636B4E756D626572267365617263685F6C616E67756167655F757365643D656E267365617263685F6D617463685F6D6F64653D6D61746368616C6C267365617263685F7061747465726E5F6D6174636865643D5E2828282872737C5253295B205D3F293F285C647B337D5B5C2D5C735D3F5C647B332C347D5B705061415D3F29297C283235285C647B387D7C5C647B317D5C2D5C647B377D29292924267365617263685F7061747465726E5F6F726465723D31267365617263685F73745F6E6F726D616C697365643D59267365617263685F726573706F6E73655F616374696F6E3D267365617263685F747970653D52535F53544F434B5F4E554D424552267365617263685F77696C645F63617264696E675F6D6F64653D4E4F4E45267365617263685F6B6579776F72643D3230332D33353339267365617263685F6B6579776F72645F6170703D32303333353339267365617263685F636F6E6669673D3026&searchHistory=%7B%22enabled%22%3Atrue%7D) which is powering the [1.5KW 220V Air Cooled Vevor Spindle](https://www.vevor.co.uk/spindle-motor-c_10130/cnc-1-5kw-air-cooled-spindle-motor-er11-engraving-inverter-mach3-pwm-mill-grind-p_010948413668?gclid=CjwKCAjwo_KXBhAaEiwA2RZ8hBkxUvOiLdsHzm8Nk6gXiaH_kTIcfACEgn4_1ap-FO-cIoHOqa5BfxoC7-0QAvD_BwE_). 

If you are not using the same setup you must review the values within the manual setup otherwise you might break either or both your spindle and inverter, this WILL make Petey sad :(

### Manual Operation

| Settings Code | Value | Description|
| ------------- |-------|---------------------  |
| P0304         | 220v  | Rated Motor Voltage [V]|
| P0305         | 7.8A  | Rated motor current [A] |
| P0307         | 1.5KW | Rated motor power [KW / hp] |
| P0308         | 0.82  | Rated motor power factor (Default=0.82) | 
| P0310         | 400   | Rated motor frequency [Hz]|
| P0311         | 24000 | Rated motor speed [RPM]   |
| P1900         | 0     | Select motor data ID      |

Now select Connection Macro `CN001` which will allow manaul operation of the motor from the inverter. 

| Settings Code | Value | Description|
| ------------- |-------|---------------------  |
| P1080         | 50    | Minimum motor frequency|
| P0305         | 400   | Maximum motor frequency |

#### Test the Spindle
1. exit the menu and press the `Green` button your spindle should spin up. 
2. To increase the speed press the `^` button. 
3. To stop the spindle press the `Red` button twice. 

#### Temperature Error - F11
You may encounter a trip followed by temperature error `F11` to fix this (disable temperature threshold) change access level and threshold by setting the following values.
| Settings Code | Value | Description|
| ------------- |-------|---------------------  |
| P8553         | 1     | Menu Type             |
| P0003         | 3     | Expert Mode           |
| P0610         | 0     | Temperature Threshold |

### RS485
Once basic settings are set and [Manual operation](#manual-operation) is working move on to this configuration.

RS485 can be used between the CNC Controller and the VDF. For this configuration I'm using the [Root Controller](https://rootcnc.com/product/root-controller-rev-2-1/)

Now select Connection Macro `CN011` which will allow RS458 operation of the motor from the inverter. 

| Settings Code | Value | Description|
| ------------- |-------|---------------------  |
| P0700         | 5     | Selection of command source            |
| P1000         | 5     | Selection of frequency                 |
| P2010         | 6     | USS/MODBUS baudrate                    |
| P2014         | 0     | USS/MODBUS telegram off time           |
| P2021         | 1     | MODBUS address                         |
| P2022         | 1000  | MODBUS reply timeout                   |
| P2023         | 2     | RS458 protocol selection               |