# DC Motor Control Project

This project demonstrates how to control a DC motor using an ATmega32 microcontroller and an L298 motor driver. The project allows for controlling the speed and direction of the motor using a potentiometer and push buttons.

## Components Used

- ATmega32 Microcontroller
- L298 Motor Driver
- DC Motor
- Potentiometer (1kΩ)
- Push Buttons (3x)
- Resistors (10kΩ x 3)
- Diodes (1N4001 x 4)
- Capacitor (100nF)
- Power Supply (12V)

## Schematic

![DC Motor Control Schematic](https://github.com/Sayed-Hossein-Hosseini/DC_Motor_Control/blob/master/AVR%20MicroController/DC%20Motor%20Control.png)

The schematic above shows the connections between the components. Here's a breakdown of the connections:

1. **Microcontroller (ATmega32)**:
    - Pins PA0-PA7: General Purpose I/O
    - Pins PB0-PB7: General Purpose I/O
    - Pins PC0-PC7: General Purpose I/O
    - Pins PD0-PD7: General Purpose I/O
    - Pin 9: RESET
    - Pins 12, 13: XTAL1, XTAL2 (for external crystal)
    - Pins 30, 32: AVCC, AREF (Analog Reference)
    - Pin 31: GND

2. **Motor Driver (L298)**:
    - Pins 1, 15: IN1, IN2 (connected to PD6, PD7 of ATmega32)
    - Pins 2, 3, 13, 14: OUT1, OUT2, OUT3, OUT4 (connected to the motor)
    - Pins 4, 12: VSS, VS (connected to 12V power supply)
    - Pins 8, 15: GND, ENA, ENB (connected to ground and control signals)
    - Pins 6, 11: SENSEA, SENSEB (connected to ground)

3. **Potentiometer (RV1)**:
    - Connected to PA0 for reading speed control

4. **Push Buttons**:
    - **Right**: Connected to PD0
    - **Left**: Connected to PD1
    - **Step**: Connected to PD2

5. **Resistors**:
    - Pull-down resistors (10kΩ) for the push buttons

6. **Diodes (1N4001)**:
    - Protection diodes for the motor driver

7. **Capacitor (100nF)**:
    - For noise filtering across the motor terminals

## Usage

1. **Speed Control**: Adjust the potentiometer (RV1) to control the speed of the DC motor.
2. **Direction Control**: Use the push buttons to control the direction of the motor:
    - **Right Button**: Rotate the motor to the right
    - **Left Button**: Rotate the motor to the left
    - **Step Button**: Step control for precise movements

## How to Run

1. **Circuit Assembly**: Assemble the circuit as per the schematic provided above.
2. **Programming**: Upload the `DC Motor Control.c` code to the ATmega32 microcontroller using an appropriate programmer.
3. **Power Up**: Connect the 12V power supply to the circuit.
4. **Operation**: Use the potentiometer and push buttons to control the motor.

## Code

The source code for this project can be found in the `DC Motor Control.c` file. It handles the reading of inputs from the potentiometer and push buttons, and controls the motor via the L298 motor driver.

## Authors

- Sayyed Hossein Hosseini
- Reza Aalaei

## License

This project is licensed under the MIT License.
