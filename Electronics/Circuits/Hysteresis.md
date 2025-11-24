24/11/2025

# Hysteresis

An overview of the Schmitter trigger/hysteresis can be found [here](/Electronics/Components/Schmitt_trigger).

To test and confirm the hysteresis affect of the schmitt triggers. A nand gate
of the 4093 chip can be used as an inverter. The differences in the thresolds
(positive-going and negative-going) can be seen.

<img src="/Images/Hysteresis.png" width="100%" >

<video width="100%" controls>
    <source src="/Images/Hysteresis_Circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

This behavious can be used in things like street lights to prevent flicker.
Here's an example circuit.
<video width="100%" controls>
    <source src="/Images/Photoresistor_hysteresis_curcuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

Hysteresis can be used to create an oscillating system.
The frequency can be calculated with 
$$ f = 1 \over RC $$
e.g. In this example, the LED will cycle just over twice a second.
$$ f = 1 \over 21,500Ω \times 0.000022F $$
$$ f = 1 \over 0.473T $$
$$ f = 2.11 $$

Where f is the frequecy at which the LED flashes
R is the resistance across the first nand gate.
C is the size of the capacitor (in farads)

The frequency can be adjusted by changing the size of the capacitor and/or
resistor.
The frequency can get so high that the LED no longer appears to flash.
If the frequency is within the range of human hearing, the LED can be swapped
out for a speaker, and the frequency can then be observed audibly.

|----------------|--------------|---------------|
| Frequency (Hz) | Resistor (Ω) | Capacitor (F) |
|----------------|--------------|---------------|
| 454.1          | 100.1kΩ      | 22nf          |
| 0.72           | 21kΩ         | 66µf          |
| 0.45           | 100.1kΩ      | 22µf          |
| 0.15           | 100.1kΩ      | 66µf          |
|----------------|--------------|---------------|

Audible with a speaker (454Hz)
<video width="100%" controls>
    <source src="/Images/Schmitt_trigger_oscillator0.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

0.72Hz
<video width="100%" controls>
    <source src="/Images/Schmitt_trigger_oscillator1.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

0.45Hz
<video width="100%" controls>
    <source src="/Images/Schmitt_trigger_oscillator2.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

0.15Hz
<video width="100%" controls>
    <source src="/Images/Schmitt_trigger_oscillator3.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 
