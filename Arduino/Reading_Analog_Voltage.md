24/10/2025

# Reading analog voltage

The give code to demo reading an analog voltage is below.

```c
/*
  ReadAnalogVoltage

  Reads an analog input on pin 0, converts it to voltage, and prints the result to the Serial Monitor.
  Graphical representation is available using Serial Plotter (Tools > Serial Plotter menu).
  Attach the center pin of a potentiometer to pin A0, and the outside pins to +5V and ground.

  This example code is in the public domain.

  https://docs.arduino.cc/built-in-examples/basics/ReadAnalogVoltage/
*/

// the setup routine runs once when you press reset:
void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(9600);
}

// the loop routine runs over and over again forever:
void loop() {
  // read the input on analog pin 0:
  int sensorValue = analogRead(A0);
  // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
  float voltage = sensorValue * (5.0 / 1023.0);
  // print out the value you read:
  Serial.println(voltage);
}
```

From this I built a simple voltage display.

## The code
```c
int led0 = 2;
int led1 = 4;
int led2 = 7;
int led3 = 8;
int led4 = 12;

void setup() {
  Serial.begin(9600);
  pinMode(led0, OUTPUT);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
}

void loop() {
  int sensorValue = analogRead(A0);
  float voltage = sensorValue * (5.0 / 1023.0);

  updateLights(voltage);
  Serial.println(voltage);
  delay(250);
}

void updateLights(int voltage) {
  int value0 = !voltage ? HIGH : LOW;
  int value1 = voltage >= 1 ? HIGH : LOW;
  int value2 = voltage >= 2 ? HIGH : LOW;
  int value3 = voltage >= 3 ? HIGH : LOW;
  int value4 = voltage >= 4 ? HIGH : LOW;

  digitalWrite(led0, value0);
  digitalWrite(led1, value1);
  digitalWrite(led2, value2);
  digitalWrite(led3, value3);
  digitalWrite(led4, value4);

}
```

## The circuit
<img src="/Images/Analog_Voltage_Reading_Circuit.jpg" width="100%" >

<video width="100%" controls>
    <source src="/Images/Analog_Voltage_Reading_Circuit.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 
## The serial output
<video width="100%" controls>
    <source src="/Images/Analog_Voltage_Reading_Serial_Output.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

## The Schematic tbc)
330Ω resistors used with each LED.
100Ω resistor used on the potentiometer.

## Questions
Was the resistor on the potentiometer required?
Were any of the resistors needed?
