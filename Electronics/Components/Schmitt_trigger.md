24/11/2025

# Schmitt triggers

Schmitt triggers use hysteresis to reduce "chatter"/oscillation.

This system can be thought of as a thermostat. In that it will turn on at a
lower bound e.g. 18°C and not turn off again until an upper bound e.g. 20°C.

With digital signals in mind, the upper half of available voltage is considered
high and the lower half is considered low.

If the circuit voltage moves around this boundary, e.g. in a 5V circuit, jumping
between 2.49V and 2.51V will cause the signal to oscillate between high and low.

The Schmitt trigger reduced this possibility by remembering the previous state
of the trigger.
e.g. if the voltage is low and increasing, the voltage must reach the positive
going threshold. In the 5v example this might be 3.5V.
if the voltage is high and reducing, this might be 1.5V.

So if the circuit is oscillating around the mid point, not change in state high
to low or vice verse will occur. The system will remain in the same state.
