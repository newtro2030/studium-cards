### Überblick

Die **Sicherungsschicht (Layer 2 / Data Link Layer)** sorgt für zuverlässige Datenübertragung zwischen **direkt verbundenen Geräten** über ein physikalisches Medium.

### Hauptaufgaben

| Aufgabe | Beschreibung |
|---|---|
| **Framing** | Bitstrom in erkennbare Rahmen (Frames) aufteilen |
| **Fehlererkennung/-korrektur** | Beschädigte Frames identifizieren, ggf. neu anfordern |
| **Flusskontrolle** | Verhindert Überlastung des Empfängers |
| **MAC (Zugriffskontrolle)** | Regelt, wer wann auf das gemeinsame Medium zugreift |

### Einordnung im OSI-Modell

```
Layer 3 – Vermittlung (Network)
Layer 2 – Sicherung (Data Link)  ← hier
Layer 1 – Bitübertragung (Physical)
```

⚠️ Layer 2 hat zwei Teilschichten:
- **LLC** (Logical Link Control) – Flusskontrolle, Fehlererkennung
- **MAC** (Medium Access Control) – Zugriff auf das Medium

### Protokolle

- **CSMA/CD** – Kollisionserkennung (Ethernet)
- **CSMA/CA** – Kollisionsvermeidung (WLAN)

> **Merksatz:** Die Sicherungsschicht organisiert Chaos – sie strukturiert, schützt und reguliert die direkte Verbindung zwischen zwei Geräten.

→ Siehe auch: [[Framing]] | [[Fehlererkennung]] | [[Fehlerkorrektur]] | [[Flusskontrolle]] | [[MAC-Sublayer]] | [[OSI- und TCP-IP-Modell]]
