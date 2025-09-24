2025/09/24

# Diodes

[Back](../README.md)

These notes need to be tidied up.
---

Diodes have a forward voltage.
Diodes have a breakdown state. The bias has been overwhelmed in the wrong direction.




As a semiconductor device, it doesn't really have such a thing as a fixed resistance. A semiconductor does different things according to different situations.

An LED is actually a type of diode, which is pretty much the simplest type of semiconductor, except that if your extent of knowledge about diodes ends at "they let current flow only in one direction", then there is a bunch of other stuff that you should know.

Firstly, below a certain voltage, a diode will effectively be "turned off" - it won't have enough voltage across its internal junction to overcome the diode's internal bias and current won't flow. Above that threshold, the diode becomes "forward biased" and current can flow. Different types of diodes have different threshold voltages where the current begins to flow - only in a trickle at first. Schottky diodes have low thresholds around 0.2V, while LEDs have thresholds around the 1.4V to 2.5V mark. The voltage at which the diode starts to conduct some significant amount of current is its "forward voltage". This will be quoted for a particular current, so for example a blue or white LED may have a forward voltage of 3.0V at around 10mA. But even though the datasheet may quote a specific figure, the actual figure varies across individual components.

You can measure this forward voltage with a multimeter. Other comments indicate how, though some multimeters have a dedicated setting. Note that because LEDs have a higher forward voltage than other diodes, your multimeter would need to supply that voltage in order for the LED to actually become forward biased, otherwise the LED will just block current. Many multimeters, unless they specify otherwise, will only use a voltage around 2V when testing resistance or in diode testing mode, and this won't be enough to switch on an LED and test its forward voltage. But others will say, as a selling point, that they use over 3V.

There are other things about diodes. If you exceed a certain voltage in the reverse direction - typically much higher than the forward voltage for example it might be 50V - you enter "breakdown" mode where the diode fails to prevent current flow and current flows in reverse over the diode. In an LED, however, the LED will be destroyed before this happens. Breakdown voltage is more relevant to other diode types. There is even a diode type called a Zener diode where the breakdown voltage is specifically engineered to be some particular voltage, so that the breakdown threshold may serve a useful purpose in your circuit.