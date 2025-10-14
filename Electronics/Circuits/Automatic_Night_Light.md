09/10/2025

# Automatic night light
Building up from a simple circuit

## Series circuits
I = V/R

When creating a simple single branch circuit the current drawn from a battery is proportional to the battery voltage, divided by the resistance of the circuit.

With a 9V battery and  a 1Ω resistor. The current is 9A. (This ignores the operational parameters of a battery - it would be a short circuit).

Increasing the resistance by 1000, to 1000Ω would reduce the current by a factor of 1000, to 0.009A (9mA).

Where the resistance comes from doesn't matter. Adding a second resistor is the same as doubling the existing resistor.

Here are some simulation and real world measurements to demostrate this.

|-------+-----------+---------------+-----------|
| Loci  | Voltage   | Resistance    | Current   |
|-------+-----------+---------------+-----------|
| Sim   | 9V        | 10,000Ω       | 900μA     |
| IRL   | 9.31V     | 9,750Ω        | 942μA     |
| Sim   | 9V        | 20,000Ω       | 450μA     |
| IRL   | 9.31V     | 19,040Ω       | 473μA     |
|-------+-----------+---------------+-----------|

## Parallel circuits
In parallel circuits, resistance calculations are different.

| Loci  | Voltage   | Resistance    | Current   |
|-------|-----------|---------------|-----------|
| Sim   | 9V        | 5,000Ω        | 1.80mA    |
| IRL   | 9.31V     | 5,180Ω        | 1.83mA    |

The measured current comes to 0.0018A (1.8mA). Which appears to go against Ohm's law.
$$ I = V/R = 9 / 20,000Ω = 0.00045A $$

The calculation for resistance in a parallel circuit is
$$ 1/R = 1/R_1 + 1/R_2 $$
$$ 1/R = {1 \over 1 / 10,000Ω + 1 / 10,000Ω} = 1 / 0.0002Ω = 5,000Ω $$ 

Using Ohm's law again now returns the simulated value.

$$ I = V/R = 9V / 5,000Ω = 0.0018A (The measured value) $$

## Voltage divider
When two components with differing resistance are in series. The voltage drop across each is proportional to their resistances.

- Simulation

|               | Resistor 1    | Resistor 2    | Both resistors    |
|---------------|---------------|---------------|-------------------|
| Resistance    | 10,000Ω       | 470Ω          | 10,470Ω           |
| Voltage drop  | 8.596V        | 0.404V        | 9V                |

- IRL
$$ %V =  9,750Ω / 10,220Ω = 95.4% $$
$$ 9.31V * 0.954 = 8.88V $$
The measured voltage of 8.87 is very close.

|               | Resistor 1    | Resistor 2    | Both resistors    |
|---------------|---------------|---------------|-------------------|
| Resistance    | 9,750Ω        | 460Ω          | 10,220Ω           |
| Voltage drop  | 8.87V         | 0.41V         | 9.31V             |

## Wheatstone bridge
The Automatice night light circuit is very similar to a Wheatstone bridge circuit.
(Created by Samuel Hunter Christie and later proposed to measure circuit resistance by Charles Wheatstone) - (Charles Wheatstone presented it as Samuel Christie's work but it is now associted with Charles).

<img src="/Images/Wheatstone_Bridge_Schematic.png" width="100%" >

A link to the math to calcultate circuit properties can be found [here](https://youtu.be/J1cBLIa5UZ4?si=rhRc3nMwtdCrBzhx). I was unable to use the math to calculate properties measured IRL.

With this circuit the direction of the current across the bridge can be manipulated by varying the resistors.

## Automatic night light
Following the above investigations specifically studying the Wheatstone bridge circuit. I have a much better understanding of the automatic night light circuit.

As the base of a semiconductor requires much less current that the collector ([Approximately 1%](https://en.wikipedia.org/wiki/2N3904).

Because of this I found that with a 9V battery the resistance of the variable resistance branch had to be at least 500 times higher than the LED branch.

<img src="/Images/Automatic_Night_Light_Schematic.png" width="100%" >
<img src="/Images/Automatic_Night_Light_My_Circuit.jpg" width="100%" >
<img src="/Images/Automatic_Night_Light_My_Circuit.mp4" width="100%" >

Limitations: The potentiometer didn't have much of an effect in adjusting the circuits sensitivity to light. I think this was becuase the range of resistance was much smaller than the

Potentiometer range: From ~9.4kΩ -> 2Ω
Compared to the two 100kΩ resistors, this isn't much.
