# About
At its core the Root controller is a ESP32 GRBL isolated motion controller (FluidNC). What makes this controller different is the focus of providing isolated IO to the CNC controller. The controller is designed to accommodate a wide range of operating conditions and machines, to provide ultimate flexibilty (its not just a Root CNC Controller).

The controller is designed to isolate the key area of the design to mintage any nuisance issues when opperating in a electrically noisey environment. The design isolates the following areas from one another. Steppers driver outputs (acheived by using externally opto isolated drivers), USB, Relays, MOSFETs and RS485. Perfectly suited for the larger CNC machines. 

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
