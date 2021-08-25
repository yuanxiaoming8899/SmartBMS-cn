# SmartBMS
Open source Smart Battery Management System
https://www.green-bms.com/smart-bms/

## Description
Smart BMS is an Open Source Battery Management System for Lithium Cells (Lifepo4, Li-ion, LTO, NCM, etc.) Battery Pack.

![alt-text](https://www.green-bms.com/wp-content/uploads/2021/06/Green_bms_functional-768x768.png)

The main functions of BMS are:
- To protect cells against overvoltage
- To protect cells against undervoltage
- To balance the cells 

Smart BMS consists of four main components:
1. Cell Module (https://www.green-bms.com/cell-module/)
2. Control Unit (https://www.green-bms.com/control-unit/)
3. Limiter (https://www.green-bms.com/limiter/)
4. Android App (https://www.green-bms.com/android-app/)

The voltage and the temperature values of each cell are acquired by the relevant Cell Module (based on Attiny microcontroller) and sent to Control Unit (based on Arduino Mega microcontroller) through a serial I2C line.

Control Unit starts or stop charging (by output relay) through Limiter, that includes a power relay for opening or closing the charging circuit.

Control Unit can also start or stop discharging by output relay.

When during charging a cell reaches the “Balance voltage value parameter”, the Cell Module connects the balance resistors in order to perform the cell bleeding.

When just one cell of the pack is balancing, Control Unit activates the current limit function inside the Limiter (the charging current is limited to 1A).

Control Unit can be connected with a Smartphone (or a Tablet) by Bluetooth.

By “Green BMS” Android app (available on Play Store)) it is possible to check the Battery Pack status (total voltage, current load, state of charge…) , to check the actual voltage and temperature values of each cell and to perform several settings.

## Tutorials

The instructions for a correct use of the BMS are enclosed in a series of video tutorials on the Youtube channel:

https://www.youtube.com/channel/UCdJnQnmzJSQNOAGbZR5iExA

Subscribe please... :smile:

- How to make Green BMS (https://www.youtube.com/watch?v=LHrENJF3j-4)
- How to set cell modules address (https://www.youtube.com/watch?v=e1lMxtpzjrA)

## Open source Development applications

The project was created using the following Open source applications:
- **Kikad** : to design cell module and Interface board
- **QElectroTech** : to design Limiter
- **Librecad 2D** : to desingn Control Unit Box
- **Arduino IDE** : to design the code of Cell Module(Attiny) and Control Unit(Arduino Mega)
- **Mit App Inventor** : to design the Android Aplication

## Warning

Lithium and other batteries are dangerous and must be treated with care.

Lithium and other batteries are potentially hazardous and can present a serious fire hazard if damaged, defective or improperly used.

Green BMS is not a professional and safety certified project.

Green BMS assumes no responsibility for any errors or inaccuracies that may appear in any documentation or file or any software that may be provided.

There is no warranty, it may not work as expected or at all.

The use of this project is done entirely at your own risk and responsibility.

The use of this project may not be compliant with local laws or regulations.

## License

This work is licensed under a **Creative Commons Attribution-ShareAlike 4.0 International License**.
https://creativecommons.org/licenses/by-sa/4.0/

### You are free to:

**Share** — copy and redistribute the material in any medium or format

**Adapt**  — remix, transform, and build upon the material
for any purpose, even commercially.
This license is acceptable for Free Cultural Works.
The licensor cannot revoke these freedoms as long as you follow the license terms.

### Under the following terms:

**Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

**ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

**No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
