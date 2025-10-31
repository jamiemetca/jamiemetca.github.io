31/10/2025

# pinMode
This is the arduino function used to set gpio pins as input or output.
The aim of this document is to drill down into how it works.

pinMode can be found in wiring_digital.c
```c
void pinMode(uint8_t pin, uint8_t mode)
{
	uint8_t bit = digitalPinToBitMask(pin);
	uint8_t port = digitalPinToPort(pin);
	volatile uint8_t *reg, *out;

	if (port == NOT_A_PIN) return;

	// JWS: can I let the optimizer do this?
	reg = portModeRegister(port);
	out = portOutputRegister(port);

	if (mode == INPUT) { 
		uint8_t oldSREG = SREG;
                cli();
		*reg &= ~bit;
		*out &= ~bit;
		SREG = oldSREG;
	} else if (mode == INPUT_PULLUP) {
		uint8_t oldSREG = SREG;
                cli();
		*reg &= ~bit;
		*out |= bit;
		SREG = oldSREG;
	} else {
		uint8_t oldSREG = SREG;
                cli();
		*reg |= bit;
		SREG = oldSREG;
	}
}
```

## Heirarchy
### Constants
- NOT_A_PIN = 0
- INPUT = 0x0;

- pinMode()
    - uint8_t
        - digitalPinToBitMask
        - digitalPinToPort
            - portModeRegister
                - \*reg
                - &=
                - ~reg
            - portOutputRegister
    - volatile
    - SREG
        - __AVR_ARCH__ in my Arduino Uno R3 it's set to 5.
    - cli();



















