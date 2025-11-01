31/10/2025

# Push button LED circuit
An example circuit provided by Arduino. Pressing a button turns on/off and LED

## Circuit overview
For this circuit we use two pins on the arduino.
- 13 as an output pin for the LED
- 2 as an input pin to detect the button press

Pin 13 is set to replicate the state of pin 2.
When pin two goes high, pin 13 is set to high.

## Circuit
<img src="/Images/Push_button_LED_tinker_cad.png" width="100%" >
Pin 2 is connected to ground via the button and the 10kΩ resistor.

This default connection pulls the pin down to ground. If it's removed the LED
behaves in an unpredictable manner, sometimes it detects a high voltage and
sometimes it detects a low voltage.

When the button is pressed, pin 2 in connected to live (high, power).
When this happens the code causes pin 13 to go high, which turns on the LED.


A simplified example of arduinos button example
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

<img src="/Images/Push_button_LED_circuit.png" width="100%" >
<video width="100%" controls>
    <source src="/Images/Push_button_LED_circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
