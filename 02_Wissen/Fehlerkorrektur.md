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

## Lernkarten

Q: Was ist der Hamming-Abstand?
A: Die **Anzahl der Bits**, die sich zwei gültige Codewörter unterscheiden. Maß für die Fehlererkennungs- und Korrekturfähigkeit eines Codes.

Q: Was kann ein Code mit Hamming-Abstand d=3?
A: **2 Fehler erkennen** und **1 Bitfehler automatisch korrigieren**.

Q: Was ist der Unterschied zwischen FEC und ARQ?
A: **FEC** (Forward Error Correction): Empfänger korrigiert Fehler lokal – kein Rückkanal nötig. Geeignet für hohe Latenz (Satelliten). **ARQ** (Automatic Repeat reQuest): Fehler erkannt → Wiederholung anfordern. Einfacher, aber verzögert.

Q: Wie funktioniert der Hamming-Code?
A: Sender berechnet **Prüfbits** an Positionen 2ⁿ (1, 2, 4, ...). Jeder Prüfbit kontrolliert bestimmte Datenbits. Der Empfänger prüft erneut – die fehlerhafte Position ergibt sich aus dem Ergebnis.
