<!--
author:   Sebastian Zug; Martin Bertau; Ines Aubel; Florian Richter; Jihad Hyadi

email:    sebastian.zug@informatik.tu-freiberg.de

version:  1.0.0

language: de

narrator: Deutsch Female

icon:     https://tu-freiberg.de/sites/default/files/styles/large_xl/public/2024-06/Logo1.png?itok=DwUdy4lK

link:     style.css

@style
.flex-container {
    display: flex;
    flex-wrap: wrap;
    align-items: stretch;
    gap: 20px;
}

.flex-child {
    flex: 1;
    margin-right: 20px;
}

@media (max-width: 600px) {
    .flex-child {
        flex: 100%;
        margin-right: 0;
    }
}

.qr {
    text-align: center;
}
@end

@qr: <img class="qr" src="https://api.qrserver.com/v1/create-qr-code/?size=220x220&data=@0" alt="QR-Code für @0" width="220" height="220">

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/Netzwerk_Westsachsen_2026/presentation.md#1)

# MyRemoteMINT

Eigene Labore für Schülerinnen und Schüler im ländlichen Raum
------------------------------------------------------------

![Remote-Labor-Stationen im RoboLab der TU Bergakademie Freiberg](./robolab_stationen.jpg)<!-- style="max-height: 28vh; width: auto; display: block; margin: 0 auto;" -->

<!-- style="font-weight: bold" -->
Prof. Dr. Sebastian Zug (Institut für Informatik), Prof. Dr. Martin Bertau (Institut für Technische Chemie) \
TU Bergakademie Freiberg \
6. Netzwerkveranstaltung „Digitale Schule Sachsen“ – Westsachsen, Schüler-Lab der WHZ Zwickau, 13. November 2026

---

> Gefördert in der Initiative Digitale Schule Sachsen, Laufzeit Juli 2026 bis Juni 2028. Dieser Vortrag ist eine Open Educational Resource (OER) unter [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de): https://github.com/IfI-MyRemoteMINT/Presentations

## Ausgangslage

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

> __Echte Experimente sind für guten MINT-Unterricht unverzichtbar.__ Sie machen Theorie anschaulich, fördern Problemlösekompetenz und begeistern für MINT-Berufe.

In der Schule stehen ihnen viele Hürden entgegen:

- Hochwertige Mess- und Robotiksysteme sind für viele Schulen zu teuer.
- Sicherheitsrelevante Experimente dürfen nicht im Klassenzimmer stattfinden.
- Labore sind nur während der Schulzeit nutzbar.
- Die Ausstattung ist ungleich verteilt, besonders im ländlichen Raum.
- Nach einem Workshop an der Hochschule bleibt an der Schule meist nichts zurück.

Das gilt für den Calliope im Informatikunterricht ebenso wie für die Messstation im Biologieunterricht oder das Fotometer in der Chemie.

</div>

<div class="flex-child" style="min-width: 250px;">

![Warum fährt der Roboter nicht?](./batteryDesaster.png "Warum fährt der Roboter nicht? Echte Hardware hat ihre eigenen Tücken.")<!-- width="80%" -->

</div>

</section>

    {{1}}
> __Unsere Frage:__ Wie bekommen alle Schülerinnen und Schüler Zugang zu echten Experimenten, unabhängig von Ort, Zeit und Ausstattung ihrer Schule?

## Remote-Labore

> __Definition:__ Remote-Labore ermöglichen den Zugriff auf echte Hardware über das Internet. Die Lernenden verändern Parameter, schreiben Programme und beobachten das Ergebnis über Kamera und Messdaten.

Im Unterschied zur Simulation zeigt ein Remote-Labor die Wirklichkeit, mit Messfehlern, Umgebungseinflüssen und allem, was dazugehört.

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

__Unsere Erfahrung seit 2017__

![Roboter des Industrial eLab](./elab_robot.png "Roboter des Industrial eLab (BMBF, 2017–2020)")
![Sechs fernsteuerbare Roboter](./elab_setup.png "Aufbau mit sechs fernsteuerbaren kleinen Robotern")
![Nutzung über die Zeit](./elab_streakmodel.png "Nutzungsverlauf einer einzelnen Person im Remote-Labor")

</div>

<div class="flex-child" style="min-width: 250px;">

__Was wir daraus gelernt haben__

- Remote-Labore funktionieren und werden intensiv genutzt.
- Aufgaben ändern konnten aber nur Fachleute.
- Server und Wartung waren aufwendig.

→ Im Projekt __CrossLab__ (2021–2025) entstand daraus __Edrys lite__: Labore aus Bausteinen, ohne Server.

</div>

</section>

## Die Idee von MyRemoteMINT

> MyRemoteMINT bringt die Remote-Labore aus der Hochschullehre in die Schulen und ergänzt sie um __mobile Hardware-Baukästen__, die __LabSets__.

| Ebene                                      | Wer betreibt das Labor?                     | Wofür?                                                                       |
| ------------------------------------------ | ------------------------------------------- | ---------------------------------------------------------------------------- |
| __1. Individuelle Remote-Labore__          | Schülerinnen und Schüler, zu Hause          | eigene Fragestellungen, angeregt durch Interesse oder Unterricht             |
| __2. Partizipative Remote-Labore__         | Lernende gemeinsam mit ihren Lehrkräften, an der Schule | Unterricht, AGs und Projektarbeiten, geöffnet auch für andere Schulen |
| __3. Zentrale Remote-Labore__              | TU Bergakademie Freiberg und BSZ „Julius Weisbach“ Freiberg | spezialisierte Experimente, die über den Lehrplan oder die Ausstattung einer Schule hinausgehen |

    {{1}}
<section>

So entsteht ein __verteiltes Labor-Netzwerk__: Schulen betreiben eigene Labore, nutzen die Angebote anderer und lernen voneinander. Alle Materialien sind __OER__ und schulübergreifend nutzbar.

> __Ziel:__ mindestens 10 aktiv beteiligte Schulen innerhalb der Projektlaufzeit.

</section>

    {{2}}
<section>

__Nicht nur Informatik__

| Fach       | Beispiele für Remote-Labore und LabSets                                      | Stand                    |
| ---------- | ---------------------------------------------------------------------------- | ------------------------ |
| Informatik | Calliope mini, Arduino, fahrende Roboter                                     | Hochschullabore vorhanden |
| Physik     | Sensorkennlinien, Distanzmessung, Analog-Digital-Wandlung                     | Hochschullabore vorhanden |
| Biologie   | Umweltsensorik (Licht, Temperatur, pH), Gewächshaus mit Portalroboter am BSZ | Gewächshaus am BSZ vorhanden, Rest geplant |
| Chemie     | elektrochemische Messungen, Chromatographie, Spektroskopie                   | geplant, mit der Technischen Chemie |

</section>

### LabSets – von Remote zu Real

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

__Beispielhafte Baukästen__

- Robotik
- Mikrocontroller
- Umweltsensorik
- elektrochemische Messungen

__Der Weg zum eigenen Labor__

1. Workshop im RoboLab Freiberg: Setups kennenlernen und ausprobieren
2. eigenen Baukasten aufbauen und als Remote-Labor einrichten
3. Baukasten bleibt an der Schule oder geht mit nach Hause
4. Labor lokal nutzen oder für andere öffnen

</div>

<div class="flex-child" style="min-width: 250px;">

__Zu jedem LabSet gehören__

- Dokumentation und Bauanleitung
- Laborbeschreibung für Edrys lite
- Beispielcode und Versuchsanleitungen
- Aufgabenblätter und Video-Tutorials

alles unter __CC BY 4.0__ und auf Git-Plattformen veröffentlicht.

> Die Lehrkräfte begleiten als Coaches und erhalten vom Projektteam technische und didaktische Unterstützung.

</div>

</section>

### Passt das in den Lehrplan?

> Wir haben die sächsischen Lehrpläne für Informatik, Physik, Chemie, Biologie, Biotechnik und Technik/Computer an Oberschule, Gymnasium und Beruflichem Gymnasium nach Anknüpfungspunkten durchsucht.

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

| Fach              | Anknüpfungspunkte |
| ----------------- | ----------------: |
| Physik            |                44 |
| Informatik        |                38 |
| Chemie            |                26 |
| Biologie          |                21 |
| Biotechnik        |                 4 |
| Technik/Computer  |                 4 |
| __Summe__         |           __137__ |

</div>

<div class="flex-child" style="min-width: 250px;">

__Beispiele__

- Informatik GY Kl. 7, Informatiksysteme: Calliope als EVA-System
- Biologie OS Kl. 9, Grundlagen der Ökologie: abiotische Faktoren digital messen
- Physik GY: verbindliche Schülerexperimente mit digitaler Messwerterfassung
- Besondere Lernleistung (BELL) und Komplexe Lernleistung: ein eigenes LabSet bauen und für andere öffnen

</div>

</section>

    {{1}}
<section>

__Nicht jedes Labor heißt programmieren.__ Dieselbe Hardware trägt vier Stufen:

| Stufe                          | Was die Lernenden tun                                        | Typische Klassen |
| ------------------------------ | ------------------------------------------------------------ | ---------------- |
| 1. Beobachten                  | Experiment starten, Live-Bild und Messwerte verfolgen        | 5–8              |
| 2. Messen und Auswerten        | Parameter variieren, Messreihen aufnehmen, Diagramme deuten  | 7–10             |
| 3. Programmieren und Modellieren | eigenen Code schreiben, Messung und Modell vergleichen     | 9–12             |
| 4. Gestalten                   | ein eigenes Experiment oder LabSet planen, bauen, freigeben  | 10–13            |

</section>

<!-- class="reference" -->
> __Quelle:__ eigene Auswertung der Lehrplandatenbank des Schulportals Sachsen, Stand Oktober 2026. Die Zuordnung ist eine Einschätzung des Projektteams und wird mit den Partnerschulen abgestimmt.

## Die Technik: Edrys lite

> __Idee:__ Ein Labor ist eine __Textdatei__, die fertige __Module__ kombiniert. Lernende brauchen nur einen Browser und einen Link.

![Remote-Labor zur Distanzmessung in Edrys lite](./edrys_distanzlabor.jpg "Remote-Labor zur Distanzmessung: Code-Editor, Kamerabild, Terminal und Aufgaben in einem Browserfenster")

    {{1}}
| [Module](https://github.com/edrys-labs) (Beispiele) | Zweck                                          |
| --------------------------------------------------- | ---------------------------------------------- |
| Markdown, LiaScript                                 | Anleitungen, Aufgaben, Quiz                    |
| Code-Editor                                         | Programmieren, gemeinsam für alle sichtbar     |
| MicroPython-/Arduino-Simulator                      | Vorbereiten und testen ohne Hardware           |
| Kamerastream                                        | Das echte Gerät beobachten                     |
| Terminal, serieller Monitor                         | Code auf das Gerät laden und ausführen         |
| Whiteboard, Chat, Umfrage                           | Zusammenarbeit und Rückmeldung                 |

### Ein Labor = eine Textdatei

```yaml   esp32_lab_de.yaml (Ausschnitt)
name: Arduino Nano ESP32 Labor
modules:
  - url: https://edrys-labs.github.io/module-markdown-it/index.html
    config:
      content: |-
        # Willkommen im Remote-Labor ...
    showInCustom: lobby

  - url: https://edrys-labs.github.io/module-monaco-editor/
    config:
      language: cpp
      runCommand: execute
    showInCustom: station

  - url: https://edrys-labs.github.io/module-streaming/index.html
    stationConfig:
      video: true
    showInCustom: station

  - url: https://edrys-labs.github.io/module-pyxtermjs/index.html
    stationConfig:
      workflow: arduino-nano-esp32
    showInCustom: station
```

    {{1}}
<section>

Was daraus folgt:

- __Ein Labor anpassen__ heißt Text bearbeiten, nicht programmieren. Das können auch Lehrkräfte und Lernende.
- __Die Hardware wechseln__ heißt wenige Zeilen ändern: Arduino, ESP32, Calliope mini oder ein Linux-Terminal.
- __Ein Labor weitergeben__ heißt eine Datei teilen, als OER.

</section>

### Ohne Server und ohne Anmeldung

> Klassische Remote-Labore brauchen eine zentrale Serverinfrastruktur. Edrys lite verbindet die Browser direkt miteinander.

``` ascii
Klassisch mit zentralem Server               Direkt von Browser zu Browser

      👨🏾‍💻 --.     .-- 👩‍💻                          - - - --👨🏾‍💻-----👩‍💻
            \   /                                              /  \
                                                              /    \
  👩‍💻 ------  🖥️  ------ 👨🏾‍💻                           👩‍💻------+-----👨🏾‍💻- - -
                                                       \    /      /
            /   \                                       \  /      /
      👨🏾‍💻 --'     '-- 👩‍💻                                  👨🏾‍💻     👩‍💻- - - -
```

    {{1}}
<section>

| Eine Station braucht ...                              | ... und keinen                          |
| ----------------------------------------------------- | --------------------------------------- |
| einen Rechner mit Chrome oder Edge                    | eigenen Server oder Cloud-Vertrag       |
| das Gerät per USB und eine Webcam                     | Portfreigaben in der Firewall           |
| bei Bedarf Docker für die Programmierwerkzeuge        | Installation auf den Schülergeräten     |

> Keine Benutzerkonten, keine zentrale Datenhaltung. Damit können Schulen ihre Labore selbst betreiben. In sehr restriktiven Schulnetzen prüfen wir die Verbindung gemeinsam vor Ort.

</section>

## Live-Demo: ein Remote-Labor in fünf Minuten

> __Zücken Sie Ihr Smartphone, Tablet oder Ihren Laptop!__

    --{{0}}--
Ich mache jetzt meinen Laptop zu einer Station. Hier am USB-Anschluss steckt ein Arduino Nano ESP32, darüber hängt eine Webcam. Genau so könnte ein LabSet an einer Schule aussehen.

1. Die Laborbeschreibung `esp32_lab_de.yaml` wird in Edrys lite geladen.
2. Ein zweites Browserfenster wird zur __Station__: Arduino Nano ESP32 per USB, Webcam auf das Board, ein Docker-Container mit `arduino-cli`.
3. Sie betreten den Klassenraum über den QR-Code unten.
4. An der Station ändern Sie den C++-Code und drücken auf Run. Der Code wird kompiliert und auf das echte Board geladen.
5. Sie sehen die RGB-LED im Kamerabild und die Ausgaben im seriellen Monitor.

    {{1}}
<section>

Für Technikinteressierte: die komplette Stationssoftware, gestartet mit einem Befehl.

``` bash
docker run -d --name edrys-station \
  -p 127.0.0.1:5000:5000 \
  --device /dev/ttyACM0 \
  -v /dev/bus/usb:/dev/bus/usb \
  --device-cgroup-rule 'c 166:* rmw' \
  --device-cgroup-rule 'c 189:* rmw' \
  edryslabs/module-pyxtermjs:latest
```

</section>

    --{{0}}--
Dieser eine Befehl ist die ganze Stationssoftware. Der Container bringt die Arduino-Werkzeuge und einen kleinen Terminal-Server mit. Der serielle Anschluss und der USB-Bus werden durchgereicht, damit der Container das Programm auf das Board laden kann.

Link zum Klassenraum der Demo:

<script input="text" placeholder="Klassenraum-URL hier einfügen" aria-label="Klassenraum-URL für die Live-Demo" style="display: block">
let url = "@input".trim()
url === ""
  ? "Fügen Sie die Klassenraum-URL ein, um den QR-Code anzuzeigen."
  : "HTML: <img src='https://api.qrserver.com/v1/create-qr-code/?size=300x300&data=" + encodeURIComponent(url) + "' alt='QR-Code für den Klassenraum' width='300' height='300'>"
</script>

## Laufende Labore in Freiberg

Diese Stationen laufen dauerhaft in unserem RoboLab. Sie sind der Ausgangspunkt für die zentralen Remote-Labore im Projekt.

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

__Calliope-mini-Labor__ (MicroPython und Sensoren, mit Simulator)

@qr(https%3A%2F%2Fedrys-labs.github.io%2F%3F%2Fclassroom%2Fj83SVIVcOd5ARUtd)

https://edrys-labs.github.io/?/classroom/j83SVIVcOd5ARUtd

</div>

<div class="flex-child" style="min-width: 250px;">

__Interrupts und Timer__ (LED-Ring)

@qr(https%3A%2F%2Fedrys-labs.github.io%2F%3F%2Fclassroom%2FsEHRNUR9TnhA8wYs)

https://edrys-labs.github.io/?/classroom/sEHRNUR9TnhA8wYs

</div>

</section>

![Calliope-mini-Labor in Edrys lite](./edrys_calliope.jpg "Calliope-mini-Labor: MicroPython-Editor, Terminal und Kamerabild der Station")

> __Und mit einer ganzen Klasse?__ Eine Station kann immer nur eine Person gleichzeitig programmieren. Deshalb arbeiten die Lernenden zuerst im Simulator und gehen dann an die Station. Mehrere gleiche Stationen laufen parallel, alle anderen schauen im Kamerabild zu. Für die zentralen Labore entsteht ein Buchungssystem.

Diese Labore stammen aus unserer Hochschullehre. Die Schulvarianten mit gestuften Aufgaben entstehen im Projekt gemeinsam mit den Partnerschulen.

## Der Fahrplan

| Phase                                   | Was passiert                                                                                       |
| --------------------------------------- | -------------------------------------------------------------------------------------------------- |
| __1. Anpassen__                         | Hochschul-Labore an Schulcurricula und Niveaustufen anpassen, Begleitmaterial mit Partnerschulen entwickeln und erproben |
| __2. Ausbauen__                         | Remote-Labore an TU Bergakademie und BSZ ausbauen, LabSets an Schulen etablieren, Projektarbeiten begleiten, Workshops und Fortbildungen im RoboLab |
| __3. Teilen__                           | Laborbeschreibungen als OER in einem durchsuchbaren Repository, Anbindung an OPAL Schule, LernSax und MeSax |

    {{1}}
> Fortbildungen für Lehrkräfte und Lernende bietet das Institut für Informatik der TU Bergakademie Freiberg auch nach Projektende an.

## Was bedeutet das für eine Schule?

| Frage                      | Antwort                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------- |
| __Technik__                | Browser auf vorhandenen Geräten; für eine eigene Station ein Rechner, das Gerät und eine Webcam |
| __Hardware__               | LabSets werden im Projekt entwickelt und beschafft und bleiben an der Schule                    |
| __Zeit__                   | Workshops von ein bis zwei Tagen im RoboLab oder vor Ort; danach Begleitung durch das Projektteam |
| __Datenschutz__            | keine Benutzerkonten, keine zentrale Datenhaltung, die Kamera zeigt nur das Gerät; die Evaluation ist datenschutzsensibel angelegt |
| __Anerkennung__            | Arbeit mit LabSets als BELL, Komplexe Lernleistung oder Projektarbeit; ein Konzept dafür entsteht im Projekt |
| __Nach 2028__              | OER bleiben frei verfügbar, LabSets bleiben an den Schulen, Workshops sollen in die Fortbildungen des LaSuB übergehen, das Institut für Informatik bietet weiter Fortbildungen an |

## Für Forschende: Begleitforschung und Kooperation

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

__Wissenschaftliche Begleitung im Projekt__

- datenschutzsensible Evaluation mit Fragebögen, Interviews und Nutzungsdaten
- Befragungen der Lernenden vor und nach der Arbeit mit den Laboren
- Usability-Studien zu Edrys lite mit Lernenden und Lehrkräften
- Veröffentlichung auf Fachtagungen, z. B. DELFI und GI-Fachtagung Bildungstechnologien

</div>

<div class="flex-child" style="min-width: 250px;">

__Was wir als Basis anbieten__

- offene Software und offene Laborbeschreibungen: Studien lassen sich an anderen Standorten wiederholen
- Module für Nutzungs- und Codeprotokolle, z. B. anonymisierte Code-Änderungen an der Station
- 137 Lehrplananker als Ausgangspunkt für fachdidaktische Fragen
- Interesse an Kooperation, besonders mit der Fachdidaktik in Biologie, Chemie und Physik

</div>

</section>

<!-- class="reference" -->
> __Bisherige Arbeiten:__ I. Aubel et al., _Adaptable Digital Labs – Motivation and Vision of the CrossLab Project_, GeCon 2022 · A. Hawlitschek, S. Berndt, S. Zug, A. Dietrich, _Iterative Adaption eines Remote-Labors unter Berücksichtigung des Feedbacks der Studierenden_, wbv

## Mitmachen

<section class="flex-container">

<div class="flex-child" style="min-width: 250px;">

__Was Ihre Schule bekommt__

- einsatzfertige Remote-Labore mit Begleitmaterial
- Workshops im RoboLab Freiberg für Lernende und Lehrkräfte
- LabSets, die an der Schule bleiben
- technische und didaktische Begleitung
- ein Netzwerk von Schulen, die voneinander lernen

</div>

<div class="flex-child" style="min-width: 250px;">

__Was wir uns wünschen__

- Lehrkräfte, die Remote-Labore im Unterricht, in AGs oder an Projekttagen erproben
- Ideen für Experimente aus Ihrem Unterricht
- Schulen, die ein eigenes LabSet aufbauen und für andere öffnen
- Lehrkräfte aller MINT-Fächer, nicht nur Informatik
- Forschende, die mit uns Fragen zu Remote-Laboren in der Schule untersuchen

__Der erste Schritt:__ Sprechen Sie uns an. Wir klären Ihre Fächer, Themen und Klassenstufen und laden Sie zu einem Workshop ein.

</div>

</section>

    {{1}}
<section>

Welches Experiment aus Ihrem Fach würden Sie gern aus der Ferne nutzen oder mit anderen Schulen teilen?

[[___ ___ ___]]

</section>

## Kontakt und Links

| Angebot                         | Link                                  |
| ------------------------------- | ------------------------------------- |
| Edrys lite und alle Labore      | https://edrys-labs.github.io          |
| Quellcode der Module und Labore | https://github.com/edrys-labs         |
| LiaScript für Begleitmaterial   | https://liascript.github.io           |
| Dieser Vortrag                  | https://github.com/IfI-MyRemoteMINT/Presentations |

__Labore selbst starten__ (es entsteht jeweils ein neuer, eigener Klassenraum):

- [Arduino-Nano-ESP32-Labor](https://edrys-labs.github.io/?/deploy/https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/Netzwerk_Westsachsen_2026/esp32_lab_de.yaml) (aus der Live-Demo)
- [Calliope-mini-Labor](https://edrys-labs.github.io/?/deploy/https://raw.githubusercontent.com/edrys-labs/lab-calliope-mini/main/lab_calliope_mini.yaml) (MicroPython, mit Simulator)

__Ansprechpartner an der TU Bergakademie Freiberg__

| Name                     | Institut                                                   | E-Mail                                   |
| ------------------------ | ---------------------------------------------------------- | ---------------------------------------- |
| Prof. Dr. Sebastian Zug  | Institut für Informatik, Softwaretechnologie und Robotik   | sebastian.zug@informatik.tu-freiberg.de  |
| Prof. Dr. Martin Bertau  | Institut für Technische Chemie                             | martin.bertau@chemie.tu-freiberg.de      |

__Projektteam:__ Dr. Ines Aubel (Institut für Technische Chemie), Florian Richter, Jihad Hyadi

<!-- class="highlight" -->
> __Projekt:__ MyRemoteMINT – Eigene Labore für Schülerinnen und Schüler im ländlichen Raum, Initiative Digitale Schule Sachsen (07/2026–06/2028), TU Bergakademie Freiberg
