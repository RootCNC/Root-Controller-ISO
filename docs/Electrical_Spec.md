# Root Controller ISO Electrical characteristics
This section is split up into the isolation zones of the controller.

For more information on the different isolation zones, please see the Wiki page tilted "Power" [Link Here](https://wiki.rootcnc.com/en/RootControllerPower)

## Primary PSU
### PSU
This is denoted a `V` and `0V_V` for supply and return respectively on the case sticker.
Power is applied through its own dedicated fused port. 

| **Parameter** | **Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|
| Vin (`V` wrt `0V_V`) | 9 |24|36|V|
|Current (Fuse Protected) (*1)|  |0.86|(*2)|A|
|Input Isolation voltage  [`V` vs `0V`(*3)]| 1.5 |||KV
-   (*1) – This is current draw of the Root CNC controller including worst case power export via output pins. This does not induce the exported power on V pins (Such as powering inductive probes)
- (*2) - Installed fuse is TBD
-  (*3) – 0V is the isolated floating voltage on the Root CNC controller – Do Not connect this to chassis

### Input
The inputs to the Root controller are referenced to the `0V_V` of the Primary PSU. All input are isolated to the rest of the system.

The Input are arranged to accept either an Open-Collector/ Open-Drain switch or a standard mechanical switch. Depending on the Primary PSU voltage this switching current will vary. 
| **Parameter** | **Condition** |**Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|--|
| Switching Current |(*1) |2.7||10|mA|
| |V = 12V ||2.7||mA|
|  |V = 24V ||5.8||mA|
|  |V = 36V ||8.9||mA|

* (1) Over full operating conditions 
# RS485 
This section is denoted by `V_RS` and `0V_RS` respectively for the Power in and 0V for the isolated RS485 port. 

| **Parameter** | **Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|
| Vin (`V_RS`wrt `0V_RS`) | 8.1 |12|36|V|
|Current Draw |  |1.6|2|mA|
|Basic DC Isolation  [`V_RS` vs `0V`]| ||1.517|KV
|Reinforced DC Insulation  [`V_RS` vs `0V`] (*1)| ||0.757|KV
|Basic bipolar AC Isolation  [`V_RS` vs `0V`] (*1)| ||565|V
|Reinforced bipolar AC Insulation  [`V_RS` vs `0V`] (*1)| ||565|V
|Differential Input Threshold Voltage, Vth|-200 |-125|-30|mV
|Input Hysteresis|| 20|| mV
|Input Resistance (A, B) (*2) |96 |150|| kΩ
|Output High Voltage|4.6|4.9||V
|Output Low Voltage||0.1|0.4|V
|Output Short-Circuit Current| 7| |85| mA
|ESD Rating (`A`,`B`)||HMB (+/-2KV)

* (1) Maximum Continuous Working Voltage
* (2) RS485 does not contain a bus termination resistor - place provisioned. The Isolating RS485 has internal thresholds to detect logic levels. 

# Digital Output
Isolation is achieved by using Opto-Isolated Stepper motor drivers

|**Parameter**|**Min**|**Typ**|**Max**|**Unit**|
|--|--|--|--|--|
|Vout (Root controller derived supply)|4.95|5|5.05|V
|Output current|||150|mA
|IOH High-level output current (*1)|||25|mA
|IOL Low-level output current (*1)|||25|mA
|VOH High-level output voltage (*2)|3.8|||V
|VOL Low-level output voltage (*3)|||0.55|V

-   (*1) This parameter makes the Root CNC controller extremely well suited to drive opto-isolated stepper motor drivers (special sauce)
-   (*2) – Over full operating specification and at max current draw (-32mA)
-   (*3) – Over full operating specification and at max current draw (32mA)

# MOSFET Isolation
The Root Controller provides three MOSFET controller switches. These switches have their own dedicated input power supply and can be driven from a separate PSU or the same PSU as `V` to allow for greater flexibility.

| **Parameter** | **Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|
| Vin (`V_F` wrt `0V_F`) | 12|15|36|V|
|Current (Fuse Protected) (*1)|0.001  ||(*2)|A|
* (1) Current is dependant of the peripherals you connect to the controller
* (2) Controller has an internal fuse - Rating is TBD

# Relay 
The Root controller has three NO relays (the Normally closed Pole is not accessible). These are design to allow the user to switch large main powered loads, such as Dust extraction, compressors and even lighting.
| **Parameter** | **Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|
| Switch Voltage DC| ||300|V|
| Switch Voltage AC| ||440|V|
|Contact Resistance|||100|mOhm|
|Switch Current (Resistive Load)|||12|A|
|Max Switch Power|||3000|VA|
|Endurance (Switch Cycles)|||1x10^7||

# USB
The USB port on the Root controller is a Type-C 2.0 UFP. This port is also isolated with the `0V`

| **Parameter** | **Min** | **Typ** | **Max** |**Unit**|
|--|--|--|--|--|
| Voltage (`V_USB` to `0V_USB`) |4.5 |5|5.5|V|
| Current| 5|8|10|mA|
| Data Rate| ||12|Mbps|
|DC Basic Isolation  |||849|V|
|AC Bipolar Basic Isolation  |||849|V|
|AC Unipolar Basic Isolation  |||560|V|