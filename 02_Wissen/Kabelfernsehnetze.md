### Hybrid Fiber Coax (HFC)

Kabelfernsehnetze verbinden **Glasfaser im Backbone** mit **Koaxialkabel zum Haushalt**.

```
Headend → Glasfaser → Fiber Nodes → Koaxialkabel → Haushalt
```

- Ursprünglich: **unidirektional** (nur Downstream – TV-Signale)
- Für Internet: **Rückkanal (Upstream)** nachgerüstet (Frequenzbereiche unterhalb TV-Kanäle)

### DOCSIS

**Data Over Cable Service Interface Specification** – Industriestandard für Internet über TV-Kabel.

| Version | Merkmal |
|---|---|
| DOCSIS 3.0 | Weit verbreitet |
| DOCSIS 3.1 | Gigabit-fähig |
| DOCSIS 4.0 | In Vorbereitung |

- Downstream: bis 1 Gbit/s und mehr
- Upstream: langsamer (50–100 Mbit/s)

### Vor- und Nachteile

| Vorteil | Nachteil |
|---|---|
| Bestehende Infrastruktur nutzbar | **Shared Medium**: Bandbreite mit Nachbarn geteilt |
| Hohe Downstream-Geschwindigkeit | **Asymmetrisch**: Upload langsamer als Download |
| Triple Play (TV, Internet, Telefon) | Störanfällig bei veralteter Verkabelung |

> **Merksatz:** Das Fernsehkabel wurde zum Internetkabel – schnell, aber gemeinsam genutzt.

→ Siehe auch: [[Übertragungsmedien]] | [[PSTN]] | [[Netzwerktypen (PAN, LAN, MAN, WAN)]]

## Lernkarten #Rechnernetze

Q: Was bedeutet HFC-Architektur?
A: **Hybrid Fiber Coax** – Glasfaser im Backbone (schnell, störarm) und Koaxialkabel im letzten Abschnitt zum Haushalt.

Q: Was ist DOCSIS?
A: **Data Over Cable Service Interface Specification** – Industriestandard für Internetübertragung über TV-Kabelnetz. Aktuell: DOCSIS 3.1 (Gigabit-fähig).

Q: Was ist der größte Nachteil von Kabelfernsehnetzen für Internet?
A: **Shared Medium** – die Bandbreite wird mit allen Nachbarn im Kabelsegment geteilt. Zudem asymmetrisch: Upload deutlich langsamer als Download.

Q: Warum wurde im Kabelnetz ein Rückkanal nachgerüstet?
A: Ursprünglich nur Downstream (TV-Signale zum Kunden). Für Internetzugang wurde ein **Upstream-Kanal** in niedrigen Frequenzbereichen hinzugefügt.
