### Was ist Framing?

Den kontinuierlichen **Bitstrom** der physikalischen Schicht in logisch erkennbare Einheiten – **Frames** – zerlegen.

**Frame-Aufbau:**
```
| Header | Nutzdaten (Payload) | Trailer (z. B. CRC) |
```

Ohne Framing: Empfänger weiß nicht, wo ein Paket beginnt/endet oder ob es korrekt ist.

### Framing-Methoden

| Methode | Funktionsweise | Vor-/Nachteil |
|---|---|---|
| **Byte Count** | Frame beginnt mit Längenfeld (Anzahl Bytes) | Einfach, aber bei beschädigtem Längenfeld Synchronisation verloren |
| **Byte Stuffing** | Frame beginnt/endet mit FLAG-Byte; FLAG in Daten wird durch ESC ersetzt | Robust, aber Codieraufwand |
| **Bit Stuffing** | FLAG-Bitmuster `01111110`; nach 5 aufeinanderfolgenden Einsen wird automatisch eine `0` eingefügt | Bit-effizient, aber komplexer |
| **Codierungsverletzung** | Nutzt physikalisch ungültige Muster als Rahmengrenzen (z. B. Manchester-Encoding) | Kein Einfluss auf Daten, aber nur bei speziellen Leitungscodes möglich |

### Bit Stuffing – Regel

- Sender: Nach jeder Folge von fünf `1`en → füge eine `0` ein
- Empfänger: Nach fünf `1`en gefolgt von `0` → entferne die `0`
- So wird das FLAG-Muster `01111110` in Nutzdaten verhindert

> **Merksatz:** Ohne Framing gäbe es nur Bitchaos – durch strukturierte Rahmen wird Kommunikation überhaupt erst möglich.

→ Siehe auch: [[Sicherungsschicht]] | [[Fehlererkennung]] | [[Ethernet (IEEE 802.3)]]

## Lernkarten #Rechnernetze

Q: Wozu dient Framing?
A: Den kontinuierlichen **Bitstrom** der physikalischen Schicht in logisch erkennbare Einheiten (**Frames**) zu zerlegen, damit der Empfänger Anfang, Ende und Korrektheit eines Pakets erkennen kann.

Q: Was sind die vier Framing-Methoden?
A: **Byte Count** (Längenfeld), **Byte Stuffing** (FLAG-Byte + ESC-Zeichen), **Bit Stuffing** (nach 5 Einsen wird 0 eingefügt), **Codierungsverletzung** (ungültige physikalische Muster als Grenze).

Q: Was ist Bit Stuffing und warum wird es verwendet?
A: Nach jeder Folge von fünf `1`en wird automatisch eine `0` eingefügt. Dadurch wird verhindert, dass das FLAG-Muster (`01111110`) in Nutzdaten auftreten kann.

Q: Woraus besteht ein Frame typischerweise?
A: **Header** (Steuerinfos, Adresse), **Payload** (Nutzdaten), **Trailer** (z. B. CRC-Prüfsumme).
