<!--
author:   Sebastian Zug
email:    sebastian.zug@informatik.tu-freiberg.de
version:  1.0.0
language: de
narrator: Deutsch Female

import:   https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md
-->

# Room 2: RGB-Lauflicht im Simulator

Bevor Sie das echte Board programmieren, probieren Sie Ihr Programm hier im Simulator aus. Der Simulator bildet einen Arduino Uno nach, an dem drei LEDs hängen: rot an Pin 13, grün an Pin 12, blau an Pin 11.

Drücken Sie auf den Ausführen-Knopf unter dem Code. Die LEDs leuchten nacheinander auf, und im Ausgabefenster erscheint der Name der Farbe.

<div id="rgb">
<wokwi-led color="red"   pin="13" label="rot (13)"></wokwi-led>
<wokwi-led color="green" pin="12" label="grün (12)"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="blau (11)"></wokwi-led>
<span id="simulation-time"></span>
</div>

``` cpp
const int leds[] = {13, 12, 11};
const char* namen[] = {"rot", "gruen", "blau"};

void setup() {
  Serial.begin(115200);
  for (int i = 0; i < 3; i++) {
    pinMode(leds[i], OUTPUT);
    digitalWrite(leds[i], LOW);   // aus
  }
}

void loop() {
  for (int i = 0; i < 3; i++) {
    digitalWrite(leds[i], HIGH);  // an
    Serial.print("Farbe: ");
    Serial.println(namen[i]);
    delay(700);
    digitalWrite(leds[i], LOW);   // aus
  }
}
```
@AVR8js.sketch(rgb)

## Aufgaben im Simulator

> **Aufgabe 1:** Lassen Sie die LEDs doppelt so schnell wechseln.

> **Aufgabe 2:** Ergänzen Sie einen vierten Schritt, in dem alle drei LEDs gleichzeitig leuchten.

> **Aufgabe 3:** Lassen Sie die rote LED `SOS` morsen (`... --- ...`): kurz = 200 ms, lang = 600 ms.

## Kurz geprüft

Was passiert im Simulator bei `digitalWrite(13, HIGH);`?

- [(X)] Die rote LED geht an.
- [( )] Die rote LED geht aus.
- [( )] Nichts, Pin 13 ist kein Ausgang.

Welche Zeile sorgt dafür, dass die Farbe im Ausgabefenster erscheint?

- [( )] `pinMode(leds[i], OUTPUT);`
- [(X)] `Serial.println(namen[i]);`
- [( )] `delay(700);`

## Weiter zur Station

Ihr Programm läuft im Simulator? Dann geht es an der **Station** auf das echte Arduino Nano ESP32.

Achtung, dort gibt es zwei Unterschiede:

1. Die LEDs heißen nicht 13, 12 und 11, sondern `LED_RED`, `LED_GREEN` und `LED_BLUE`.
2. Die RGB-LED des Nano ESP32 ist **LOW-aktiv**: `LOW` schaltet sie ein, `HIGH` schaltet sie aus. Genau umgekehrt wie hier im Simulator.

Woran merken Sie an der Station, wenn Sie `HIGH` und `LOW` vergessen haben zu tauschen?

[[___ ___ ___]]
