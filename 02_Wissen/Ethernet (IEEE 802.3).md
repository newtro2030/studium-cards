### Überblick

Ältestes und am weitesten verbreitetes LAN-Protokoll. Entwickelt in den 1970ern (Xerox/DEC/Intel), 1983 als **IEEE 802.3** standardisiert.

Entwicklung: Bus-Topologie mit Koaxialkabel → Twisted Pair + Stern-Topologie mit Switches.

### Ethernet-Frame-Format

| Feld | Größe | Funktion |
|---|---|---|
| Präambel | 7 Byte | Synchronisation |
| SFD | 1 Byte | Start Frame Delimiter |
| Zieladresse | 6 Byte | MAC-Adresse des Empfängers |
| Quelladresse | 6 Byte | MAC-Adresse des Senders |
| Typ/Länge | 2 Byte | Protokolltyp (z. B. IPv4) |
| Nutzdaten | 46–1500 Byte | Payload |
| CRC | 4 Byte | Fehlererkennung (32-Bit CRC) |

**Mindestlänge:** 64 Byte (inkl. Header & CRC)

### MAC-Adressen

- 48-Bit (6 Bytes), z. B. `08:00:27:12:AB:CD`
- **Unicast**: eindeutiger Empfänger
- **Broadcast**: alle Stationen (`FF:FF:FF:FF:FF:FF`)
- **Multicast**: Gruppe von Empfängern

### Switched Ethernet

Moderne Switches **trennen Kollisionsdomänen** → kein CSMA/CD mehr nötig → Vollduplexbetrieb möglich.

### Versionen

| Version | Geschwindigkeit | Medium |
|---|---|---|
| 10BASE-T | 10 Mbit/s | Twisted Pair |
| 100BASE-TX | 100 Mbit/s | Twisted Pair |
| 1000BASE-T | 1 Gbit/s | Twisted Pair |
| 10GBASE-LR | 10 Gbit/s | Glasfaser |
| 100GBASE-ER4 | 100 Gbit/s | Glasfaser |

> **Merksatz:** Ethernet hat sich vom geteilten Koaxialkabel zum Gigabit-Backbone entwickelt – schnell, skalierbar, universell.

→ Siehe auch: [[MAC-Sublayer]] | [[Sicherungsschicht]] | [[Übertragungsmedien]] | [[OSI- und TCP-IP-Modell]]
