22/10/2025

# Traffic light with an arduino

This is the C code for the arduino Uno to run 3 LEDs in a traffic light
sequence.

```C
int red = 5;
int amber = 6;
int green = 7;

void setup() {
  pinMode(red, OUTPUT);
  pinMode(amber, OUTPUT);
  pinMode(green, OUTPUT);
}

void loop() {
  digitalWrite(amber, LOW);
  digitalWrite(red, HIGH);
  delay(3000);

  digitalWrite(amber, HIGH);
  delay(2000);

  digitalWrite(red, LOW);
  digitalWrite(amber, LOW);
  digitalWrite(green, HIGH);
  delay(5000);

  digitalWrite(green, LOW);
  digitalWrite(amber, HIGH);
  delay(2000);
}
```

<video width="100%" controls>
    <source src="/Images/Traffic_Lights_Arduino_My_Circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
