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
- [Capacitor](../Electronics/Components/Capacitor.md)
    - (22uf - mircofarads and 22nf nanofarads) 
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
## Notes

### TODO
- Add frequency calculation to formula page.
    - 1 second/ time (time for 1 wave cycle)  = frequency

- PicoScope

- 230V * 1.4(RMS value) = 320V

- half-wave rectifier- AC -> DC

- Diode
    - current goes towards the silver stripe
    - Voltage drop
        - 0.71 - This number comes up alot
        - The voltage lost across a diode
        - It's a side-effect
        - P-N junction - this drop is what consumes the power.

- On Amazone (Ali-express ~ £3)
    - buy a kit to build your own signal generator
    - requires soldering
    - 

- Capacitors
    - T = RC
        - Add time to discharge calculation to formula page.
    - Capacitance is how much charge is stored per volt.
    - What is meant by a polarised capacitor?
        - This means it can only be connected in one direction.
        - What happens if it's connected the wrong way and why?
    - Ripple voltage
        - The capacitor can't charge quickly enough.
        - This occurs when the power is drawn quickly enough between phases that the capacitor begins to discharge.
    - Shark fin graph
        - Multiple the time factor by 5 to get an idea of how long a capacitor will take to discharge.
            - Will it take the same amout of time to charge?
    - They are timing circuits
        - Toasters
        - Bathroom fans
        - Car interior lights

- Voltage
    - What is considered low?
    - Does it depend on the current?
    - Can you SAFELY measure the resistance of you (the capacitor was discharging through his body)

-  R-C network
    - r= r per v
    - c = c per volt
T = RC

- Transistor
    - Why does the resistor on the base affect the brighnes of the LED

- MOSFET
    - The base is activated by voltage. No current needs to flow.
    - They are also sensitive, and so can be damaged by static electricity.
        - Be sure to use the ESD strap before handling.

- TODO
    - Review the tasks
    - Write ups;
        - Circuits covered
            - Create schematics for all the circuits built.
            - Upload images and video
        - Components covered
            - Update existing notes with additional notes
            - Create notes for new components
    - Investigate the dimming circuit further.
        - What affect does changing each of the resistors have?

## Task- charge and capacitor (22uF)
- Measure the voltage
- Observe discharging
- Comment on time taken to discharge

Notes on capacitors [here](/Electronics/Components/Capacitors.md)

$$ T = RC $$
Where;
- T = Time constant
- R = Resistance
- C = Capacitance
 
I measured the following.
- The capacitor has 23.2μF.
- The resistance was 23.54kΩ.
Convert to base units.
$$ 23.2μF = 23.2 \times 10^{-6} = 0.0000232F $$
$$ 23.54kΩ = 23.54 \times 10^{3} = 23,540Ω $$
$$ T = R \times C = 23,540Ω \times 0.0000232F = 0.546 seconds $$

Following the time constant table I'd expect 36.8% of max voltage after 0.546 seconds. (3.24V)

This is not what I saw: It took 4 minutes and 21 seconds (261 seconds) to go from 9V to 3.24V (~36% of max).

My error: I was measuring the discharge with the DMM in series which significantly increased the resistance of the circuit.

I modified the circuit to measure the voltage in parallel and the discharge time dropped.
After approximately 1 second, which is approximately 2 time constanct units, the voltage was about 1.2V which is very close to the expected 1.24V (2T = 13.5%)

<img src="/Images/Charge_Discharge_And_Measure_Capacitor_Voltage_My_Circuit.jpg" width="100%" >

## Task- Build and assess the Automatic night light circuit
- Meaure the gain (hFE) of the transistor.


- Measure the voltages in the circuit
    - Transistor base voltage (between base and 0V) when on and off
    - Transistor collector voltage (between collector and 0V) when on and off
    - LED voltage when on and off
    - Any other voltages to check

[Write up](/Electronics/Circuits/Automatic_Night_Light.md)
