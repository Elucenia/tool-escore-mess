<!-- ELUCENIA technical documentation · escore-mess · de · no clinical/professional/rights approval -->

# MESS (Schweregradscore für schwer verletzte Extremitäten)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/escore-mess)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Skelett- und Weichteilverletzung

`energia`

- `1` — Niedrige Energie (Stichverletzung, einfache Fraktur, Kurzwaffenprojektil)
- `2` — Mittlere Energie (offene oder multiple Fraktur, Luxation)
- `3` — Hohe Energie (Hochgeschwindigkeitsunfall, Gewehrprojektil)
- `4` — Sehr hohe Energie (wie oben + grobe Kontamination)

### Extremitätenischämie

`isquemia`

- `0` — Keine Ischämie
- `1` — Verminderter oder fehlender Puls, normale Perfusion
- `2` — Kein Puls, Parästhesien, verlangsamte Kapillarfüllung
- `3` — Kalte, gelähmte, gefühllose Extremität

### Ischämie seit mehr als 6 Stunden?

`tempo`

- `0` — Nein
- `1` — Ja

### Schock

`choque`

- `0` — Systolischer Blutdruck immer \> 90 mmHg
- `1` — Vorübergehende Hypotonie
- `2` — Anhaltende Hypotonie

### Alter

`idade`

- `0` — \< 30 Jahre
- `1` — 30 bis 50 Jahre
- `2` — \> 50 Jahre

## Fassung der Methode

MESS/Johansen 1990: 4 Domänen, Ischämie verdoppelt \>6 h; keine automatische Amputationsanordnung

## Dokumentierte Formel

MESS = Skelett-/Weichteilverletzung (1 bis 4) + Ischämie (0 bis 3, verdoppelt bei Dauer über 6 h) + Schock (0 bis 2) + Alter (0 bis 2).

## Grenzen und Population

Der ursprüngliche MESS wurde in kleinen Gruppen mit schwerem Trauma der unteren Extremität entwickelt. Die Verbindung der Schwelle ≥7 mit Amputation in diesen Gruppen ist weder universelle Regel noch automatische Indikation. Gliedmaßenerhalt hängt von multidisziplinärer Beurteilung und nicht im Score zusammengefassten klinischen Bedingungen ab.

## Referenzen

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

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
