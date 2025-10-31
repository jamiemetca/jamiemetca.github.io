31/10/2025

# Drilling down into Arduino's code

Here is simplified arduino code to turn on an LED when a buton is pressed.
```c
const int buttonPin = 2;
const int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  int buttonState = digitalRead(buttonPin);

  digitalWrite(ledPin, buttonState);
}

```

The pinMode function can be copied to the root file.
```c
const int buttonPin = 2;
const int ledPin = 13;

void setup() {
  myPinMode(ledPin, OUTPUT);
  myPinMode(buttonPin, INPUT);
}

void loop() {
  int buttonState = digitalRead(buttonPin);

  digitalWrite(ledPin, buttonState);
}

void myPinMode(uint8_t pin, uint8_t mode)
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


