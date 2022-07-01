---
title: Pin numbering
description: Root Controller ISO Program pin numbers
published: true
date: 2022-05-29T20:56:11.673Z
tags: root controller
editor: markdown
dateCreated: 2022-03-14T22:22:48.038Z
---
# Root Controller ISO Pin mapping

> This list support the revision 2.0 Onwards. If you're after an earlier version pin out please see the version history on Github 
{.is-info}

# I2S Output Port Mapping
I2S Bus is purely outputs ONLY.
|**Port**| **Description**|**Port**| **Description**|**Port**| **Description**|**Port**| **Description**|
|--|--|--|--|--|--|--|--|--|--|
|**I2S_0**	|X_EN_PIN          |**I2S_8**|Z_EN_PIN          |**I2S_16**|	SPINDLE_DIR    |**I2S_24**|	B_EN_PIN       |
|**I2S_1**	|X_DIRECTION_PIN   |**I2S_9**|Z_DIRECTION_PIN   |**I2S_17**|	SPINDLE_EN     |**I2S_25**|	B_DIRECTION_PIN|
|**I2S_2**	|X_STEP_PIN        |**I2S_10**|	Z_STEP_PIN     |**I2S_18**|	SPARE_1        |**I2S_26**|	B_STEP_PIN     |
|**I2S_3**	|X_CS - NOT USED   |**I2S_11**|	Z_CS - NOT USED|**I2S_19**|	SPARE_2        |**I2S_27**|	B_CS - NOT USED|
|**I2S_4**	|Y_EN_PIN          |**I2S_12**|	FET_1          |**I2S_20**|	A_EN_PIN       |**I2S_28**|	C_EN_PIN       |
|**I2S_5**	|Y_DIRECTION_PIN   |**I2S_13**|	RELAY_1        |**I2S_21**|	A_DIRECTION_PIN|**I2S_29**|	C_DIRECTION_PIN|
|**I2S_6**	|Y_STEP_PIN        |**I2S_14**|	RELAY_2        |**I2S_22**|	A_STEP_PIN     |**I2S_30**|	C_STEP_PIN     |
|**I2S_7**	|Y_CS - NOT USED   |**I2S_15**|	RELAY_3        |**I2S_23**|	A_CS - NOT USED|**I2S_31**|	C_CS - NOT USED|

# ESP32 Mapping
|**Port**| **Description**|**Port**| **Description**|**Port**| **Description**|
|--|--|--|--|--|--|
|**GPIO2**|Y-PIN        	|**GPIO17**|RS_485_TX     |**GPIO27**|PROBE-PIN  |  
|**GPIO4**|RS_485_DE_RE 	|**GPIO18**|SD_CLK        |**GPIO32**|B-PIN       | 
|**GPIO5**|SD_CS        	|**GPIO19**|SD_MISO       |**GPIO33**|FET_2        |
|**GPIO12**|SHIFT_DATA   	|**GPIO21**|SHIFT_STR_CLK |**GPIO34**|GRBL_MACRO   |
|**GPIO13**|FET_3        	|**GPIO22**|SHIFT_CLK     |**GPIO35**| A-PIN       |
|**GPIO14**|C-PIN        	|**GPIO23**|SD_MOSI       |**GPIO36**|GRBL_HOLD    |
|**GPIO15**|Z-PIN        	|**GPIO25**|DAC_OUT/PWM   |**GPIO39**|GRBL_START   |
|**GPIO16**|RS_485_RX    	|**GPIO26**|X-PIN         |||

