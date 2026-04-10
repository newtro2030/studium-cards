### Ziel

Nicht nur erkennen, sondern **automatisch korrigieren** – ohne Frame erneut zu senden. Besonders nützlich bei hoher Latenz (Satelliten) oder eingeschränktem Rückkanal.

### Grundidee: Redundanz

Sender fügt **zusätzliche Bits (Redundanz)** hinzu → Empfänger kann Fehler lokalisieren und korrigieren.

### Hamming-Abstand

Anzahl der Bits, die sich zwei gültige Codewörter unterscheiden.

| Hamming-Abstand (d) | Erkennt | Korrigiert |
|---|---|---|
| d = 1 | keine Sicherheit | keine Korrektur |
| d = 2 | 1 Fehler | keine Korrektur |
| d = 3 | 2 Fehler | 1 Bitfehler |
| d = 4+ | Mehrfacherkennung | je nach Code |

### Hamming-Code

- Sender berechnet **Prüfbits** an Positionen 2^n (1, 2, 4, 8, ...)
- Jeder Prüfbit kontrolliert eine Kombination von Datenbits
- Empfänger prüft Prüfbits → fehlerhafte Position ergibt sich aus dem Ergebnis
- Einzelbitfehler wird **automatisch korrigiert**

### FEC vs. ARQ

| Verfahren | Beschreibung | Wann geeignet |
|---|---|---|
| **ARQ** (Automatic Repeat reQuest) | Fehler erkannt → Wiederholung anfordern | Einfacher Rückkanal vorhanden |
| **FEC** (Forward Error Correction) | Fehler lokal beim Empfänger korrigiert | Echtzeitübertragung, hohe Latenz, kein guter Rückkanal |

> **Merksatz:** Fehler erkennen ist gut – Fehler automatisch beheben ist besser.

→ Siehe auch: [[Fehlererkennung]] | [[Flusskontrolle]] | [[Sicherungsschicht]]
