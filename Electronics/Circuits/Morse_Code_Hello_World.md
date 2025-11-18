[Back](../)

23/10/2025

# Morse code Hello world

Below is the code and a demo video of a text to morse code coverter running
on the arduino.

```C
char* alphabet[] = {
  ".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ".---", "-.-", ".-..", "--",
  "-.", "---", ".--.", "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--.."
};
char dash = '-';
int baseDelayTime = 750;
float dashDelay = .75;
float dotDelay = .25;

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  parseText("hello");
  Serial.println();

  parseText("world");
  Serial.println();
}

void parseText(char* word) {
  while(*word != '\0') {
    char* morseLetter = alphabet[*word++ -97];
    stringToFlash(morseLetter);
    Serial.print(' ');
  }
}

void stringToFlash(char letter[]) {
  while(*letter != '\0') {
    Serial.print(*letter);

    float fraction = *letter++ == dash ? dashDelay : dotDelay;
    flash(baseDelayTime * fraction);
  }
  delay(baseDelayTime);
}

void flash(float pause) {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(pause); 
  digitalWrite(LED_BUILTIN, LOW);
  delay(pause);
}
```

<video width="100%" controls>
    <source src="/Images/Morse_Code_Hello_World.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
