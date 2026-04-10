### Warum Fehlererkennung?

Bits können durch Rauschen, Dämpfung oder Hardwaredefekte umkippen. Die Sicherungsschicht muss erkennen, ob ein Frame **fehlerhaft** angekommen ist.

⚠️ **Fehlererkennung ≠ Fehlerkorrektur** – hier geht es nur um Erkennung → ggf. Neuanforderung.

### Methoden

| Verfahren | Funktionsweise | Erkennt |
|---|---|---|
| **Paritätsbit** | Zählt 1-Bits; fügt Bit hinzu damit Gesamtanzahl gerade/ungerade ist | Einzelbitfehler; nicht alle Mehrfachfehler |
| **Prüfsumme (Checksum)** | Addiert 16-Bit-Blöcke; Gesamtsumme soll 0 ergeben | Viele Fehler, aber nicht alle; leicht zu implementieren |
| **CRC** | Modulo-2-Division durch Generatorpolynom; Rest wird angehängt | Alle Einzel- und Doppelfehler, alle ungeraden Bitfehler, Burstfehler bis Generatorlänge |

### CRC – Cyclic Redundancy Check

```
Sender:   Daten ÷ Generatorpolynom → CRC-Rest anhängen
Empfänger: (Daten + CRC) ÷ Generatorpolynom → Rest ≠ 0 → Fehler
```

- Datenblock als **binäres Polynom** behandelt
- Modulo-2-Division (kein Übertrag)
- Extrem zuverlässig bei geringer Komplexität
- Verwendet in: Ethernet, WLAN, USB

> **Merksatz:** Fehler passieren – wichtig ist, dass wir sie erkennen, bevor sie Schaden anrichten.

→ Siehe auch: [[Fehlerkorrektur]] | [[Framing]] | [[Sicherungsschicht]]
