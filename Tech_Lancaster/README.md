02/10/202

# Logbook

[Home](/)

# Week three 30/09/2025
Weeks one and two were meet and greet and had no lab work.

- Find a web based circuit simulator.
    - everycircuit
        - Looks really good but requires payment for any circuits that are not really basic (e.g. 1 LED, 1 resistor)
    - tinkerCad
        - Not as clean as every circuit but so far has remained free.

## Task 1
---
#### Be able to identify all of the components
- Can information be gleaned from type numbers?
#### How does the potentiometer work?
#### State the differences between transistors and MOSFET
#### How are the four pins on the switch connected?

- 4093 IC
- [555 timer](../Electronics/Components/555_Timer.md)
- 9V battery
- Antistatic write strap
- Arduino Uno
- Battery snap
- Breadboard
- Capacitor (22uf - mircofarads and 22nf nanofarads) 
- DMM (digital multimeter)
- [LED](../../Electronics/Components/LEDs.md)
- [MOSFET (N channel)](../Electronics/Components/Mosfet.md)
- [Potentiometer](../Electronics/Components/Potentiometer.md)
- Resistors
- [Switch](../Electronics/Components/Switch.md)
- LDR (Light dependant resistor)
- Piezo
- [Thermistor](../Electronics/Components/Thermistor.md)
- [Transistors](../Electronics/Components/Transistor.md)
- [Diode](../Electronics/Components/Diodes.md)
- Wires

## Task 2
---
#### Identify all SMD (surface mounted devices) on both sides of the Arduino
- Identify any through hole components? (Are there any)

## Task 3
---
#### Build an LED power indicator circuit

<img src="/Images/Single_LED_Circuit.png" width="100%" >
<img src="/Images/Single_LED_My_Circuit.jpg" width="100%" >

#### Add another LED in parallel

<img src="/Images/Two_LEDs_Circuit.png" width="100%" >
<img src="/Images/Two_LEDs_My_Circuit.jpg" width="100%" >

#### Ensure the correct resistors are being used
- I found the voltage drop of an LED was around 1.8V and 2.2V for a red and green LED respectively.

$$ Red LED: {9V - 1.8V \over 0.02A} = {7.2V \over 0.02A} = {360Ω} $$
$$ Green LED: {9V - 2.2V \over 0.02A} = {6.8v \over 0.02A} = {340Ω} $$

- We were advised to use the next step up in available resistors. Which in our kit is 470Ω.

## Task 4
---
#### Measure voltages across the LEDs and resistors

<img src="/Images/Two_LEDs_Circuit.png" width="100%" >
<img src="/Images/Two_LEDs_My_Circuit.jpg" width="100%" >

The component voltages are;
- Battery: 9.27V
- Green LED: 2.16V
- Resistor (of the green LED): 6.69V
- Green branch total: 2.16V + 6.69V = 8.87V
- Red LED: 1.98V
- Resistor (of the red LED): 6.95V
- Red branch total: 1.98V + 6.95V = 8.93V

#### Do the component voltages sum to the power supply voltage?

I'm missing about ~
$$ (9.27V - 8.87V) + (9.27V - 8.93V) = .4V + .34V = 0.74V $$

## Task 5 and Task 6
---
#### Calculate current (I) with 470 and 1000 ohm resistors.
- $$ I= {V_R /over R_R}$$
- Where V_R = Voltage of resistor
- Where R_R = Resistance of resistor
#### Measure the current with the DMM on the 200mA range.

<img src="/Images/Single_LED_Circuit.png" width="100%" >
<img src="/Images/Single_LED_My_Circuit.jpg" width="100%">
$$ {V_R /over R_R} = { 6.69V /over 470Ω } = 0.01423A (14.23mA) $$
- The measured value of 14.58mA (milli amps) is almost exactly what I expected.

<img src="/Images/Two_LEDs_Circuit.png" width="100%" >
<img src="/Images/Single_LED_Two_470_resistors_My_Circuit.jpg" width="100%" >
- The supplied 1kΩ resistor is actullay 330Ω so I'll calculate two 470Ω resistors in series.

$$ {V_R /over R_R} = { 7.13V /over 470Ω /times 2 } = {7.13V /over 940Ω} = 0.0076A (7.6mA)  $$
- The measured value of 7.64mA is almost exactly as expected.

## Task 7 and Task 8
---
#### Replace the resistor with the LDR
#### Measure the resistance of the LDR (light dependant resistor).
#### Record the maximum and minimum resistances (vary the light level)?

<img src="/Images/Single_LED_LDR_My_Circuit.jpg" width="100%" >

<video width="100%" controls>
    <source src="/Images/Single_LED_LDR_My_Circuit.TS.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 


#### No light (covered sensor)
$$ { V /over I } = { 7.45V /over 0.00036A } = 20,694Ω $$

#### Ambient light
$$ { V /over I } = { 7.35V /over .00144A } = 5,104Ω $$

#### No light (covered sensor)
$$ { V /over I } = { 7.21V /over .0062A } = 1,163Ω $$

### Additional tasks
Confirm the resistor ratings are correct.

|-------|-------|-----------|
| Label | Bands | Measured  |
|-------|-------|-----------|
| 1000  | 330   | 322       |
| 470   | 470   | 461       |
| 22    | 10000 | 96000     |
| 10    | 22000 | 21400     |
|-------|-------|-----------|

# Week four 07/10/2025

