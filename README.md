# MyRemoteMINT – Vorträge und Informationsmaterial

Vorträge und Handouts des Projekts **MyRemoteMINT – Eigene Labore für Schülerinnen und Schüler im ländlichen Raum** der TU Bergakademie Freiberg, gefördert in der Initiative Digitale Schule Sachsen (Juli 2026 bis Juni 2028).

Die Vorträge sind [LiaScript](https://liascript.github.io)-Kurse. Ein Klick auf **Vortrag starten** öffnet sie direkt im Browser, ohne Installation. Die Remote-Labore basieren auf [Edrys lite](https://edrys-labs.github.io).

## Vorträge

| Datum      | Anlass                                                                                         | Vortrag                                                                                                                                                                                                                                                                   | Material                                                                                                                         |
| ---------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 13.11.2026 | 6. Netzwerkveranstaltung „Digitale Schule Sachsen“ – Westsachsen, Schüler-Lab der WHZ Zwickau | [![Vortrag starten](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/Netzwerk_Westsachsen_2026/presentation.md) | [Infoblatt (PDF)](Netzwerk_Westsachsen_2026/infoblatt/infoblatt.pdf) · [ESP32-Labor](Netzwerk_Westsachsen_2026/esp32_lab_de.yaml) · [Simulation](https://liascript.github.io/course/?https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/Netzwerk_Westsachsen_2026/esp32_simulation.md) · [Quelltext](Netzwerk_Westsachsen_2026/presentation.md) |

Neue Vorträge stehen oben in der Tabelle.

## Einen neuen Vortrag ergänzen

1. Einen Ordner nach dem Muster `Anlass_Jahr` anlegen, zum Beispiel `Lehrerfortbildung_Freiberg_2027`, und darin die Datei `presentation.md` sowie alle Bilder ablegen.
2. In der Tabelle oben eine neue Zeile **über** den bisherigen einfügen. Der Startlink folgt immer diesem Muster:

   ```
   https://liascript.github.io/course/?https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/<Ordner>/presentation.md
   ```

3. Lokal ansehen mit `liascript-devserver --input presentation.md --live` im Ordner des Vortrags.

Hinweise zum Schreiben:

- Tabellen bekommen `<!-- data-type="none" -->` in die Zeile davor, damit LiaScript keine Diagramme daraus macht.
- Nach einem Push dauert es oft ein paar Minuten, bis GitHub die neue Fassung ausliefert. LiaScript speichert Kurse zusätzlich im Browser; bei Bedarf mit Strg+Shift+R neu laden.

## Lizenz

Alle Inhalte stehen unter [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de), soweit nicht anders angegeben.

## Kontakt

Prof. Dr. Sebastian Zug (Institut für Informatik) und Prof. Dr. Martin Bertau (Institut für Technische Chemie), TU Bergakademie Freiberg
