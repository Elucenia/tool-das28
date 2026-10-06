<!-- ELUCENIA technical documentation · das28 · de · no clinical/professional/rights approval -->

# DAS28 (BSG und CRP)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/das28)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Druckschmerzhafte Gelenke (von 28)

`tjc`

Bereich: 0–28

### Geschwollene Gelenke (von 28)

`sjc`

Bereich: 0–28

### Globale Gesundheitsbeurteilung durch den Patienten (visuelle Skala)

`gh`

mm · Bereich: 0–100

### Blutsenkungsgeschwindigkeit (BSG)

`vhs`

mm/h · optional · Bereich: 1–150

### C-reaktives Protein (CRP)

`pcr`

mg/L · optional · Bereich: 0–300

## Fassung der Methode

DAS28-BSG/Prevoo 1995 und DAS28-CRP/Wells 2009; 28 Gelenke; CRP-Achsenabschnitt 0,96

## Dokumentierte Formel

DAS28-BSG = 0,56 × √(druckschmerzhaft) + 0,28 × √(geschwollen) + 0,70 × ln(BSG) + 0,014 × globale Beurteilung.

DAS28-CRP = 0,56 × √(druckschmerzhaft) + 0,28 × √(geschwollen) + 0,36 × ln(CRP + 1) + 0,014 × globale Beurteilung + 0,96 (CRP in mg/L).

## Grenzen und Population

DAS28 von 1995 wurde für die Aktivität rheumatoider Arthritis anhand der Zählung von 28 Gelenken und Vergleichen mit der klinischen Beurteilung durch Rheumatologen entwickelt. Die CRP-Variante ist nicht automatisch der BSG-Variante gleichwertig; Formel, Einheiten und Schwellen müssen zur verwendeten Quelle und Ausgabe passen.

## Referenzen

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Mäßige Aktivität der rheumatoiden Arthritis


### 2

Remission der rheumatoiden Arthritis


### 3

Hohe Aktivität der rheumatoiden Arthritis


### 4

Mäßige Aktivität der rheumatoiden Arthritis

Der DAS28-CRP ergibt in der Regel niedrigere Werte als der DAS28-ESR: Bei denselben Grenzwerten kann die Remission überschätzt werden.

