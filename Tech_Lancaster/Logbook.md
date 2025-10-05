02/10/2025 (last updated 03/10/2025)

# Logbook

[Home](/)

## TL1P1

### Task 1
- Be able to identify all of the components
    - Can information be gleaned from type numbers?
- How does the potentiometer work?
- How are the four pins on the switch connected?
- State the differences between transistors and MOSFET

- [LED](../../Electronics/Components/LEDs.md)
- Resistors
- [MOSFET (N channel)](../Electronics/Components/Mosfet.md)
- [Thermistor](../Electronics/Components/Thermistor.md)
- [Transistors](../Electronics/Components/Transistor.md)
- [Potentiometer](../Electronics/Components/Potentiometer.md)
- [Switch](../Electronics/Components/Switch.md)
- [555 timer](../Electronics/Components/555_Timer.md)
- LDR (Light dependant resistor)
- Capacitor (22uf - mircofarads and 22nf nanofarads) 
- [Diode](../Electronics/Components/Diodes.md)
- Piezo
- Arduino Uno
- 4093 IC
- 9V battery
- Battery snap
- Wires
- Antistatic write strap
- DMM (digital multimeter)
- Breadboard

### Task 2
    - Identify all SMD (surface mounted devices) on both sides of the Arduino
    - Identify any through hole components? (Are there any)

### Task 3
    - Build an LED power indicator circuit

<img src="/Images/Single_LED_Circuit.png">

    - Add another LED in parallel

<img src="/Images/Two_LEDs_Circuit.png">

    - Ensure the correct resistors are being used
        
I found the voltage drop of an LED was around 1.8V and 2.2V for a red and green LED respectively.

$$ Red LED: {9V - 1.8V \over 0.02A} = {7.2V \over 0.02A} = {360Ω} $$
$$ Green LED: {9V - 2.2V \over 0.02A} = {6.8v \over 0.02A} = {340Ω} $$

We were advised to use the next step up in available resistors. Which in our kit is 470Ω.

### Task 4
    - Measure voltages across the LEDs and resistors
        - Do the component voltages sum to the power supply voltage?

### Task 5
    - Calculate current (I) with 470 and 1000 ohm resistors.
        - $$ I= {V_R /over R_R}$$
        - Where V_R = Voltage of resistor
        - Where R_R = Resistance of resistor

### Task 6
- Measure the current with the DMM on the 200mA range.

### Task 8 - Re-ordered tasks
- Replace the resistor with the LDR

### Task 7
- Measure the resistance of the LDR (light dependant resistor).
- Record the maximum and minimum resistances (vary the light level)?
