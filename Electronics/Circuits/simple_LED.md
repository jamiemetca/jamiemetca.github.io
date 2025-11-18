[Back](../)

2025/09/20 (last update 29/09/2025)

# Simple LED circuit

## Objective:
- To calculate the resistor value required to prevent damage to an [LED](../Components/LEDs.md)
- To draw a circuit schematic
- To construct a circuit
- To measure and create notes on
  - Voltage
    - Across the battery
    - Across the LED
    - Across the resistor
    - Across differnt parts of the circuit
  - Current (amps)
    - Coming from the battery
    - At different parts of the circuit
  - Resistance (ohms)
    - Of the LED
    - Of the resistor
- To gain real world experience constructing and testing circuits.

## Design & Components
### Circuit Description:

A breadboard with a 9v battery connected via a battery clip. With 1 LED and resistor in series. All connected via jumper wires

### Schematic: TODO

- Bill of Materials (BOM):
  - Components
    - Breadboard
    - 9v battery
    - 9v battery clip connector
    - [LED](../Components/LEDs.md)
    - Resistor
    - Jumper wires

## Measurements & Testing

Planned Measurements
- LED
  - Voltage: 1.6V - 2.2V
  - Expected Value: I expect the resistance of the LED to be
  - Reasoning: This is the standard resistance of basic LEDs
 - Parameter: - Measured Value: - Observations: Note any differences from your expected values and any issues encountered.

Reflections & Follow-Up
 - Summary: What were the main takeaways? What went well, and what was challenging?
 - Next Steps: What modifications or future projects would you like to pursue based on this circuit?

## Notes
To calculate the resistor needed to protect the LED the following information was required
$$ R = {V_s - V_f \over I_f} = {9V - 1.2V \over 0.02A} = {7.8v \over 0.02A} = {390Ω} $$
Where;
  - R = resistance (the resistor value we want)
  - $V_s$ The Supply voltage
  - $V_f$ The LEDs forward voltage
  - $If$ The LEDs forward current (operating current)
  - Forward voltage
    - The minimum voltage required for current to flow
  - Forward current
    - The operating current range
  - 
