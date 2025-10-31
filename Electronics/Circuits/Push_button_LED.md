31/10/2025

# Push button LED circuit
An example circuit provided by Arduino. Pressing a button turns on/off and LED

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
