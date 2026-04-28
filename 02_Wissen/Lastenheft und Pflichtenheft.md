Im deutschsprachigen Raum werden *Lastenheft* und *Pflichtenheft* unterschieden (DIN 69901-5, VDI Richtlinie 251, V-Modell XT).

### Lastenheft
- Beschreibung der Anforderungen aus **Auftraggeber-Innensicht**
- Typischerweise Element einer Ausschreibung
- Zusammenfassung aller fachlichen Basisanforderungen und Rahmenbedingungen
- Fokus: **"Was"**, nicht "Wie" (keine Vorgaben zur Realisierung)
- Zusätzlich: **Glossar** mit Erklärung wichtiger Begriffe

#### Aufbau Lastenheft (nach H. Balzert)
1. **Visionen und Ziele** - Was soll durch das Produkt erreicht werden?
2. **Rahmenbedingungen** - Anwendungsbereiche und [[Stakeholder]]
3. **Kontext und Überblick** - Produktumgebung festlegen
4. **Funktionale Anforderungen** - Kernfunktionalitäten auf oberster Abstraktionsebene
5. **Qualitätsanforderungen** - Nichtfunktionale Anforderungen (Benutzbarkeit, Effizienz, etc.)

#### Qualitätsanforderungen (Beispiel)

| Produktqualität | sehr gut | gut | normal | irrelevant |
| :--- | :---: | :---: | :---: | :---: |
| Funktionalität | | X | | |
| Zuverlässigkeit | | | X | |
| Benutzbarkeit | | X | X | |
| Effizienz | | | X | |
| Wartbarkeit | | | X | |
| Portabilität | | | | X |

#### Sprache im Lastenheft
- Natürliche Sprache: flexibel, einfach, universell verständlich
- Problem: Sprache ist **mehrdeutig/fehlerträchtig**
- Lösung: Glossar + **strukturierte Sprache und Anforderungsschablonen**

#### Anforderungsschablone
Aufbau: `[Subjekt] + [Verbindlichkeit] + [ggf. Bedingung] + [Objekt] + [Prozesswort]`

Verbindlichkeitsstufen:
- **muss** - zwingende Anforderung
- **soll** - dringende Empfehlung
- **sollte in Zukunft** - optionale Anforderung

### Pflichtenheft
- Detaillierte Beschreibung der Anforderungen aus **Anbieter-/Auftragnehmer-Innensicht**
- Umsetzung des Lastenhefts, typischerweise Angebot
- Fokus: **"Wie"** werden die Anforderungen realisiert

### Zusammenhang
- Lasten- und Pflichtenheft können auch zusammengefasst werden (bspw. als **SRS-Dokument** = Software Requirements Specification)

```
Problem analysieren → "Warum?"
    ↓
Anforderungen bestimmen → Lastenheft → "Was?"
    ↓
Anforderungen spezifizieren → Pflichtenheft → Entwurf → "Wie?"
```

→ Siehe auch: [[Anforderungsanalyse]] | [[Machbarkeitsstudie]]
