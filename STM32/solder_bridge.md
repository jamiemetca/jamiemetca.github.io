25/11/2025

# Solder bridge SB

Solder bridges are small pads on the PCB that can be permanently connnected (ON)
or left unconnected (OFF) using solder or a small resistor. They are typically
used for selecting configurations that are rarely changed.

 ## SB1 (OFF - is default)
SB1 controls the connection of the MCU's reset line
- This means the reset signal from the on-baord ST-LINK debugger/programmer
is disconnected from the target MCU's reset pin.
- In it's default configuration (quick-start) the ST-LINK controls the reset
line for debugginer and programming.
- Only set SB1 to ON if using an external debugger or need to isolate the
reset line.

## SB14 (ON - internal regulator)
- SB14 controls the connection of the internal voltage regulator outpu (Vdd_mcu)
to the 3.3V power line of the board.
- ON is the default. The internal voltage regulator is actively supplying the
3.3V power to the MCU.
- SB14 needs to be on to power the MCU correctly.
