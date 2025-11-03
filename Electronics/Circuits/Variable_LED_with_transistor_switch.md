03/11/2025

# Variable dimming LED with transistor

This circuit uses an analog in and analog out pin.

The in pin (A0) measures voltage change of a potentiometer.

The out pin (9) outputs a analog signal which I use to incrementally increase
the current to the base pin of a transistor.

<img src="/Images/Varianle_LED_transistor_circuit.jpg" width="100%" >

<video width="100%" controls>
    <source src="/Images/Varianle_LED_transistor_circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

This is a round about circuit as the change in voltage could be used directly.
I also should have used a resistor on the base pin of the transistor to protect
it.

I tried to add a seperate 9V battery via the collector and emitter pins of the
transistor. Which did work. But there is now a timing issue with the arduino
meaning I can't upload a new sketch.
