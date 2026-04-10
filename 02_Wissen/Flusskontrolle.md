### Ziel

Verhindert, dass der **Sender schneller Daten sendet**, als der Empfänger verarbeiten oder puffern kann → sonst: Pufferüberlauf, Datenverlust, Netzwerküberlastung.

### Stop-and-Wait

```
Sender → [Frame] → Empfänger
Sender ←  [ACK]  ← Empfänger
Sender → [Frame] → ...
```

- **Einfach, zuverlässig**
- **Ineffizient** bei hoher Latenz: Leitung während Wartezeit unausgelastet

### Sliding Window

Mehrere Frames **gleichzeitig im Umlauf** halten, ohne auf jedes ACK zu warten.

| Begriff | Bedeutung |
|---|---|
| **Sequenznummer** | Jeder Frame ist nummeriert |
| **Fenstergröße** | Max. Anzahl unbestätigter Frames gleichzeitig |
| **ACK** | Positiv – Frame erfolgreich empfangen |
| **NACK** | Negativ – Fehler signalisiert |

**Vorteil:** Bessere Leitungsauslastung, anpassbar an Latenz-Bandbreite-Produkt.

### Fehlerbehandlung (ARQ-Strategien)

| Variante | Verhalten bei Fehler |
|---|---|
| **Go-Back-N** | Alle Frames ab dem fehlerhaften werden wiederholt |
| **Selective Repeat** | Nur der fehlerhafte Frame wird neu gesendet (Puffer nötig) |

⚠️ **Selective Repeat** ist effizienter, aber aufwändiger (Empfänger muss puffern).

> **Merksatz:** Flusskontrolle ist wie ein Tempolimit im Netzwerk – sie verhindert Datenstaus und Zusammenbrüche.

→ Siehe auch: [[Sicherungsschicht]] | [[Fehlerkorrektur]] | [[MAC-Sublayer]]

## Lernkarten

Q: Wozu dient Flusskontrolle?
A: Verhindert, dass der **Sender schneller sendet**, als der Empfänger verarbeiten/puffern kann → sonst Pufferüberlauf und Datenverlust.

Q: Wie funktioniert Stop-and-Wait?
A: Sender sendet **einen Frame**, wartet auf **ACK**, sendet erst dann den nächsten. Einfach und zuverlässig, aber ineffizient bei hoher Latenz.

Q: Was ist das Sliding-Window-Protokoll?
A: Mehrere Frames dürfen gleichzeitig „im Flug" sein. Jeder Frame hat eine **Sequenznummer**. Der Empfänger sendet kumulative ACKs. Die **Fenstergröße** gibt an, wie viele unbestätigte Frames erlaubt sind.

Q: Was ist der Unterschied zwischen Go-Back-N und Selective Repeat?
A: **Go-Back-N**: Alle Frames ab dem fehlerhaften werden wiederholt. **Selective Repeat**: Nur der fehlerhafte Frame wird neu gesendet (Empfänger muss puffern – effizienter).
