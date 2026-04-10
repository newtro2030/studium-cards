### Problem

Wenn mehrere Benutzer ein **gemeinsames Übertragungsmedium** teilen, muss geregelt werden: **Wer darf wann senden?**

### Statische Kanalzuweisung

Kanal wird **fest und dauerhaft** aufgeteilt.

| Verfahren | Beschreibung |
|---|---|
| **FDM** (Frequency Division Multiplexing) | Jeder Nutzer bekommt einen Frequenzbereich |
| **TDM** (Time Division Multiplexing) | Jeder Nutzer bekommt einen Zeitslot |

- **Vorteil:** Einfach, vorhersehbar
- **Nachteil:** Ineffizient wenn Nutzer ungleich aktiv sind

### Dynamische Kanalzuweisung

Kanalnutzung wird **flexibel** angepasst je nach aktuellem Bedarf.

| Typ | Beschreibung | Vor-/Nachteil |
|---|---|---|
| **Zentralisiert** | Zentrale Steuerinstanz koordiniert Zugriffe | Optimale Planung, aber Einzelpunkt-Ausfall |
| **Dezentralisiert** | Teilnehmer entscheiden unabhängig (probabilistisch) | Robust, skalierbar, aber Kollisionsgefahr |

### Verfahren im Überblick

| Verfahren | Merkmal |
|---|---|
| **ALOHA** | Sendet jederzeit ohne Koordination |
| **Slotted ALOHA** | Zeitslots → weniger Kollisionen |
| **CSMA/CD** | Lauscht vor dem Senden, bricht bei Kollision ab |
| **CSMA/CA** | Vermeidet Kollisionen durch Wartezeiten |

> **Merksatz:** Ein gemeinsames Medium braucht klare Regeln – sonst reden alle durcheinander.

→ Siehe auch: [[ALOHA-Protokolle]] | [[MAC-Sublayer]] | [[Ethernet (IEEE 802.3)]] | [[WLAN (IEEE 802.11)]]

## Lernkarten

Q: Was ist der Unterschied zwischen statischer und dynamischer Kanalzuweisung?
A: **Statisch**: Feste Zuweisung (FDM, TDM) – einfach, aber ineffizient bei ungleicher Nutzung. **Dynamisch**: Flexibel je nach Bedarf – effizienter, aber komplexer und kollisionsgefährdet.

Q: Was ist FDM und was ist TDM?
A: **FDM** (Frequency Division Multiplexing): Jeder Nutzer bekommt einen eigenen Frequenzbereich. **TDM** (Time Division Multiplexing): Jeder Nutzer bekommt einen Zeitslot.

Q: Was ist der Nachteil zentralisierter dynamischer Kanalzuweisung?
A: **Einzelpunkt-Ausfall** und Verzögerungen, da alle Zugriffe durch eine zentrale Instanz koordiniert werden müssen.
