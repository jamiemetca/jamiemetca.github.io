2025/09/25 (last updated 29/09/2025)

# Formula

[Back](README.md)

## Symbols
- I = current (amperes)
- P = power (watts)
- R = resistance (ohms)
- V = voltage (volts)

## Ohm's law
$$ V = I \times R | I = V / R | R = V / I $$

## Current (I)
$$ I = V / R $$
$$ I = P / V $$
$$ I = \sqrt{P / R} $$

## Power (P)
$$ P = V^2 / R $$
$$ P = I^2 \times R $$
$$ P = I \times V $$

If the circuit has parallel branches and you know the resistance of the components. You can use this to find the approximate power of each component
$$ R_{component} / R_{branch} \approx P $$

## Resistance (R)
$$ R = V / I $$
$$ R = V^2 / P $$
$$ R = P / I^2 $$

### Calculating resistor required for LED circuit
$$ R = {V_s - V_f \over I_f} = {9V - 1.2V \over 0.02A} = {7.8v \over 0.02A} = {390Ω} $$
- R = resistance
- $V_s$ The Supply voltage (battery)
- $V_f$ The LEDs forward voltage
- $If$ The LEDs forward current (operating current)

## Voltage (V)
$$ V = I \times R $$
$$ V = \sqrt{P \times R} $$
$$ V = P / I $$
