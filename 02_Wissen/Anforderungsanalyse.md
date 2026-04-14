## Anforderungsanalyse (Requirements Engineering)

In der Anforderungsanalyse wird festgelegt, **was** die zu entwickelnde Software leisten soll – jedoch noch **nicht** der Lösungsweg dahin. Es ist der Prozess der Erhebung, Beschreibung und Analyse von Anforderungen.

> "The hardest single part of building a software system is deciding precisely what to build. [...] No other part of the work so cripples the resulting system if done wrong." *(F. Brooks, 1987)*

### Teilprozesse der Anforderungsanalyse
1. Zusammenarbeit und Dialog mit Stakeholdern
2. **Erhebung** (*Requirements Elicitation*)
3. **Analyse** (*Requirements Analysis*)
4. **Dokumentation** (*Requirements Specification*)
5. **Überprüfung** (*Requirements Validation*)
6. **Verwaltung** (*Requirements Management*)

→ Iterativer Prozess in Zusammenarbeit und Dialog mit [[Stakeholder|Stakeholdern]]

### Anforderungen (Requirements)

> "Requirement: (1) A condition or capability needed by a user to solve a problem or achieve an objective. (2) A condition or capability that must be met or possessed by a system or a system component to satisfy a contract, standard, specification, or other formally imposed documents." *(IEEE 620.12, 1990)*

- **Funktionale Anforderungen**: Definition bereitzustellender Funktionen und Dienste der Software bzw. deren Ein-/Ausgabeverhalten
- **Nichtfunktionale Anforderungen**: weitere Bedingungen, die das vollständige Softwaresystem betreffen:
  - *Produktanforderungen*: Benutzbarkeit, Effizienz, Zuverlässigkeit, Portabilität
  - *Organisatorische Anforderungen*: Umsetzungsvorgaben, Standards
  - *Externe Anforderungen*: rechtliche, ethische Anforderungen
- Klassifikation der Anforderungen oft nach Wichtigkeit (**Priorisierung**)

### Stakeholder
- **Auftraggeber**: finanzielle Interessen, oft nicht identisch mit Anwendern
- **Anwender**: Interesse an Arbeitserleichterung, evtl. Widerspruch zu Auftraggeberwünschen
- **Auftragnehmer**: Interesse an effizientem und gewinnbringendem Projekt
- **Entwickler**: ehrgeizige Lösung, möglichst wenig Aufwand

### Erhebungsmethoden
- **Interviews** (strukturiert/unstrukturiert)
- **Umfragen** (geschlossen/offen)
- **Beobachtung, Rollenspiele** (gelebte vs. vorgeschriebene Arbeitsabläufe)
- **Prototyping** (Papier oder Software)
- **Szenarien, Use/Misuse Cases, Storyboarding**
- Brainstorming, Workshops, Dokumentenanalyse, Reverse Engineering

### Validierung von Anforderungen
Fehler in der Anforderungsanalyse sind sehr teuer → Prüfung wichtig!

Prüfkriterien:
- **Validität**: Wurden die richtigen Anforderungen erfasst?
- **Konsistenz**: Sind die Anforderungen widerspruchsfrei und realisierbar?
- **Vollständigkeit**: Fehlen wichtige Funktionen?
- **Machbarkeit**: Unter realistischer Zeit/Kosten realisierbar?
- **Überprüfbarkeit**: Lässt sich die Realisierung prüfen (Abnahme)?
- **Verfolgbarkeit**: Ist der Ursprung der Anforderungen nachvollziehbar?
- **Verständlichkeit** und **Änderbarkeit**

Methoden zur Anforderungsprüfung:
- Prüf-/Analysewerkzeuge (Widerspruchsfreiheit, Vollständigkeit)
- *Reviews* zur systematischen manuellen Prüfung
- *Prototyping* zur Analyse von Validität oder Machbarkeit

### Zehnerregel der Fehlerkosten
- Fehler werden häufig in frühen Phasen verursacht
- Fehler werden oft erst spät (oder gar nicht) entdeckt
- Kosten für Beseitigung steigen in späteren Phasen exponentiell (ca. **1:100** von Analyse bis Post-Release)

### Aufgaben der Phase
- Festlegung der geforderten Softwareeigenschaften:
  - Funktionalität, Leistung, Portierbarkeit
  - Zeitverhalten, Hardwareanforderungen, Benutzerschnittstelle
- Bestimmen von Testfällen
- Festlegung notwendiger Dokumentationen

### Ergebnisse (Artefakte)
- **[[Lastenheft und Pflichtenheft|Lastenheft]]** (vom Auftraggeber): beschreibt Erwartungen des Auftraggebers
- **[[Lastenheft und Pflichtenheft|Pflichtenheft]]** (vom Auftragnehmer): beschreibt wie die Anforderungen realisiert werden
- Akzeptanztestplan
- Entwurf Benutzungshandbuch

### Einordnung im Wasserfallmodell
- Vorherige Phase: [[Machbarkeitsstudie]]
- Nächste Phase: [[Softwareentwurf]]

### Einordnung im V-Modell
- Entspricht der [[Systemanforderungsanalyse|Systemanforderungsanalyse]]
- Wird validiert durch: [[Abnahme und Nutzung]]
