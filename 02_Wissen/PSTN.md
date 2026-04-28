### PSTN – Public Switched Telephone Network

Das **öffentliche Vermittlungstelefonnetz** – ursprünglich analog, heute größtenteils digitalisiert. Dient Sprach- und Datenübertragung.

### Struktur

| Komponente | Funktion |
|---|---|
| **Local Loop** | Verbindung Haushalt ↔ Vermittlungsstelle (meist Kupfer/Twisted Pair) |
| **Vermittlungsstellen** | Aufbauen, Halten, Abbauen von Verbindungen (hierarchisch: lokal → regional → Backbone) |
| **Multiplexing** | Mehrere Gespräche auf einer Leitung |
| **Modulation** | Wandlung digitaler Signale in übertragbare Frequenzen (Modem) |

### Multiplexing-Verfahren

| Verfahren | Typ | Beschreibung |
|---|---|---|
| **FDM** | Frequency Division Multiplexing | Analog, verschiedene Frequenzbänder |
| **TDM** | Time Division Multiplexing | Digital, Zeitschlitze |

### Digitalisierung

- Früher: rein analog (Analogtelefonie)
- Heute: Backbone digital (ISDN, Glasfaser, digitale Vermittlungsstellen)
- Endgeräte können weiterhin analog sein – Umsetzung erfolgt im Netz

### PSTN und Internet

- PSTN = Grundlage früher Modem-Einwahlverbindungen
- **DSL**: nutzt bestehende Telefonleitungen für Breitbandinternet
- **VoIP**: IP-basierte Telefonie ersetzt PSTN zunehmend

> **Merksatz:** Das Telefonnetz war der Ursprung der weltweiten Kommunikation – heute trägt es Daten, nicht nur Stimmen.

→ Siehe auch: [[Übertragungsmedien]] | [[Mobilfunk]] | [[Kabelfernsehnetze]]

## Lernkarten #Rechnernetze

Q: Was ist der Local Loop im PSTN?
A: Die Verbindung vom **Hausanschluss bis zur nächsten Vermittlungsstelle** – meist aus Kupferdraht (Twisted Pair). Kann Analog- oder DSL-Signale übertragen.

Q: Was ist der Unterschied zwischen FDM und TDM?
A: **FDM** (Frequency Division Multiplexing): Analog, verschiedene Frequenzbänder gleichzeitig. **TDM** (Time Division Multiplexing): Digital, Zeitschlitze für verschiedene Signale.

Q: Wie wird das Internet über PSTN-Leitungen realisiert?
A: Über **DSL** (Digital Subscriber Line) – nutzt bestehende Telefonleitungen für Breitbandinternet. Heute ersetzt **VoIP** zunehmend die klassische Telefonie.

Q: Wie ist das PSTN hierarchisch aufgebaut?
A: 1. **Lokale Vermittlungsstelle** → 2. **Tandem-/Regionalknoten** → 3. **Backbone-Knoten** (Landes-/Fernverbindungen).
