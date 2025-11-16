15/11/2025

# Nand gate push button circuits
A simple circuit to demonstrate a nand gate.
Both buttons need to be pressed to turn off the LED.

<img src="/Images/Nand_Buttons_Circuit_Schematic.png" width="100%" >
As shown the position of the pull down resistors don't matter. In that they are
only required to prevent a short circuit.


<img src="/Images/Nand_Buttons_Circuit.jpg" width="100%" >

<video width="100%" controls>
    <source src="/Images/Nand_Buttons_Circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 


## Hysterisis in circuits

Hysterisis means the circuit has memory. The circuits switching point (the input
voltage that causes the out to change) is different depending on whether the
input voltage in increasing or decreasing.

So the circuit has an;
- upper threshold, the input voltage required for the output
to switch from low to high.
- Lower threshold: the input voltage requried for the output to switch from high
to low.

Uses of this are handling bouncing in switches.

Street light sensors. To prevent flickering.

<img src="/Images/Hysterisis_Circuit.jpg" width="100%" >
<img src="/Images/Hysterisis_Circuit_2.jpg" width="100%" >

As can be seen. The point at which the LED turns off, is lower than the point at which it turns on.

<video width="100%" controls>
    <source src="/Images/Hysterisis_Circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

