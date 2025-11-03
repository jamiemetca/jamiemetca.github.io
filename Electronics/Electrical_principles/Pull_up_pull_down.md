02/11/2025

# Pull up/down
Some parts of some circuits need to be pulled up or down, depending on their
desired behaviour.

In the [push button circuit](/Electronics/Circuits/Push_button_LED) pin 2, which
causes pin 13's behaviour to change depending on it's own state.
e.g. if it's input is high, it sets pin 13's output to high and vise versa.

To achieve this, pin 2 is connected to ground when the button is not pressed
and connect to [VCC](/Electronics/Acronyms) (5V).

If pin 2 was not connected to ground it would be undefined. The effect of this
could be pin 13, unexpectedly being set to high.

<img src="/Images/Pull_up_pull_down_resistors_schematic.webp" width="100%" >

## Pull up
The wire/component is connected to VCC via a resistor by default and a switch
is used to connect it to ground.
This has the effect of pulling the target component up until the switch is
flipped.

## Pull down
The component is connected to ground via a resistor by default. And a switch
is used to connected the component to VCC. This will pull the component to
ground by default.
