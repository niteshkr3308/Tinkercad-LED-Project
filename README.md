# Tinkercad LED Project

This project demonstrates interfacing 8 LEDs with an Arduino Uno and  blinking patterns.

[View the Tinkercad project here](https://www.tinkercad.com/things/0uYO7zBcxar-swanky-wluff?sharecode=VaZuU8D2fnIN7Nqrhd0VDaNrPKE6A-t9SC-elnHJY2I)

## Code
```cpp
const int ledPins[] = {0, 1, 2, 3, 4, 5, 6, 7, 8};
const int numLeds = 8;

void setup() {
  
  for (int i = 0; i < numLeds; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(ledPins[i], HIGH);
    delay(50); 
    digitalWrite(ledPins[i], LOW);
    delay(50);
  }
}
