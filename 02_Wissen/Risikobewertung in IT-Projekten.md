# Risikobewertung in IT-Projekten

Besonders bei **größeren IT-Projekten** ist ein systematisches Risikomanagement zwingend erforderlich, um potenzielle Gefahren frühzeitig zu erkennen, zu bewerten und Gegenmaßnahmen (Mitigation) zu planen. 

### Das schrittweise Vorgehen

Die Risikobewertung ist Teil des Risikomanagements und läuft in der Regel wie folgt ab:
1. **Risikoidentifikation**: Sammeln aller denkbaren Risiken (z. B. durch Checklisten, Brainstorming, Architekturanalyse, Experteninterviews).
2. **Risikobewertung (Qualitativ/Quantitativ)**: Jedes identifizierte Risiko wird anhand von zwei Dimensionen eingeschätzt:
   - **Eintrittswahrscheinlichkeit (P)**
   - **Schwere der Auswirkung / Schadensausmaß (k)**
   Aus diesen beiden Größen ergibt sich das Gesamtrisiko (oft als `R = P * k` modelliert).
3. **Maßnahmenplanung**: Was tun wir dagegen? (Risiko vermeiden, vermindern, auf Dritte abwälzen z. B. durch Versicherung, oder bewusst akzeptieren).
4. **Risikoüberwachung**: Eignen sich die Maßnahmen? Haben sich Wahrscheinlichkeiten im Projektverlauf geändert?

### Die Risiko-Matrix

Zur visuellen und quantitativen Einordnung nutzt man üblicherweise eine Risiko-Matrix. 

*Aufbau*:
- **y-Achse (Schwere, k)**: Pfeil von oben nach unten (von gering zu hoch)
- **x-Achse (Wahrscheinlichkeit, P)**: Pfeil von links nach rechts (von gering zu hoch)

| Schwere (k) ↓ \ Wahrscheinlichkeit (P) → | Gering | Mittel | Hoch |
| :--- | :--- | :--- | :--- |
| **Gering** | Geringes Risiko (Grün) | Geringes Risiko (Grün) | Mittleres Risiko (Gelb) |
| **Mittel** | Geringes Risiko (Grün) | Mittleres Risiko (Gelb) | Hohes Risiko (Rot) |
| **Hoch** | Mittleres Risiko (Gelb) | Hohes Risiko (Rot) | Kritisches Risiko (Rot) |

**Bedeutung der Risikostufen:**
- 🟢 **Grün (Gering)**: Risiko wird dokumentiert und akzeptiert ("Restrisiko"). Keine sofortigen proaktiven Maßnahmen zwingend erforderlich, aber es wird im Auge behalten.
- 🟡 **Gelb (Mittel)**: Es sollten Maßnahmen zur Risikominimierung (Wahrscheinlichkeit senken oder Schaden begrenzen) geplant werden.
- 🔴 **Rot (Hoch/Kritisch)**: Akuter Handlungsbedarf vor oder während des Projekts! Ohne Gegenmaßnahmen ist der Projekterfolg stark gefährdet.

> **Merksatz**: Ein Risiko ist immer das Produkt aus der Wahrscheinlichkeit, dass etwas schiefgeht, und dem Schmerz (Ausmaß), wenn es passiert.

→ Siehe auch: [[Softwareentwicklung]] | [[Machbarkeitsstudie]] | [[Vorgehensmodell]]

## Lernkarten

Q: Warum ist Risikomanagement besonders bei größeren IT-Projekten wichtig?
A: Um potenzielle Gefahren, die im Verlauf großer, komplexer Projekte auftreten können, frühzeitig zu erkennen, zu bewerten und proaktiv Gegenmaßnahmen einleiten zu können, bevor sie den Projekterfolg gefährden.

Q: Welche zwei zentralen Faktoren werden bei der Risikobewertung für jedes Risiko ermittelt?
A: 1. Die **Eintrittswahrscheinlichkeit (P)** (Wie wahrscheinlich ist es, dass das Ereignis eintritt?) und 2. die **Schwere der Auswirkung / das Schadensausmaß (k)** (Welchen Schaden richtet es an?).

Q: Wie ist eine einfache Risiko-Matrix aufgebaut?
A: Auf der X-Achse wird die **Eintrittswahrscheinlichkeit (P)** (gering zu hoch) und auf der Y-Achse die **Schwere (k)** (gering zu hoch) aufgetragen. Durch die Kombination ergeben sich Risikostufen: z. B. niedrig (Grün), mittel (Gelb) und hoch/kritisch (Rot).
