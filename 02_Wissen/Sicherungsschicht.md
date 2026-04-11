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

## Lernkarten #Rechnernetze

Q: Welche vier Hauptaufgaben hat die Sicherungsschicht?
A: **Framing** (Bitstrom strukturieren), **Fehlererkennung/-korrektur**, **Flusskontrolle** (Empfänger nicht überfordern), **MAC** (Zugriff auf gemeinsames Medium regeln).

Q: Erläutere den Unterschied zwischen Dienst (Service) und Protokoll im OSI-Modell.
A: **Dienst**: Vertikale Kommunikation innerhalb eines Geräts (was eine Schicht der darüberliegenden anbietet). **Protokoll**: Horizontale Kommunikation zwischen gleichrangigen Schichten auf verschiedenen Geräten (Regelwerk).

Q: Nenne ein Beispiel für einen Service zwischen Netzwerkschicht (L3) und Sicherungsschicht (L2).
A: Ein Beispiel ist die **Anforderung zur Übertragung eines Datenpakets** (z. B. `DL-Unitdata.Request`). Die Schicht 3 übergibt ein Paket an Schicht 2 und erwartet dessen zuverlässige (oder unbestätigte) Übermittlung zum Nachbarknoten.

Q: Beschreibe den ARP-Prozess beim Übergang von Schicht 3 zu Schicht 2.
A: 1. Sender kennt IP (L3), braucht aber MAC (L2) für den Frame. 2. Sender schickt **ARP-Request** als Broadcast (`FF:..:FF`) mit der Ziel-IP. 3. Der Ziel-Host erkennt seine IP und antwortet mit einem **ARP-Reply** (Unicast) inklusive seiner MAC-Adresse. 4. Der Sender speichert die MAC im ARP-Cache und kann den Frame adressieren.

Q: Welche OSI-Schichten sind Layer 1, 2 und 3?
A: Layer 1: Bitübertragung (Physical). Layer 2: Sicherung (Data Link). Layer 3: Vermittlung (Network).
