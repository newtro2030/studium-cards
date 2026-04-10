### Aufgabe

In Netzwerken mit **gemeinsam genutztem Medium** (Ethernet, WLAN) muss geregelt werden, **welche Station wann senden darf** – um Kollisionen zu vermeiden oder zu behandeln.

### Taxonomie der MAC-Protokolle

| Kategorie | Beschreibung | Beispiele |
|---|---|---|
| **Kollisionsfrei** | Medium wird streng zugewiesen | TDM, Token Passing |
| **Kollisionserkennung** | Sender erkennt Kollision beim Senden | CSMA/CD (Ethernet) |
| **Kollisionsvermeidung** | Sender vermeidet Kollisionen vorher | CSMA/CA (WLAN) |

### CSMA/CD (Ethernet)

1. Kanal lauschen (Carrier Sense)
2. Wenn frei → senden
3. Beim Senden weiter lauschen
4. Kollision erkannt → **Jamming Signal** senden, aufhören
5. Zufällige Wartezeit (Backoff), dann neuer Versuch

⚠️ Nur für **kabelgebundene Netze** mit Halbduplex. Nicht für WLAN.

### CSMA/CA (WLAN)

1. Kanal prüfen
2. Wenn frei → **zufällige Wartezeit**
3. Dann senden
4. Optional: **RTS/CTS** (Request to Send / Clear to Send) gegen Hidden Node Problem

### Vergleich

| Merkmal | CSMA/CD | CSMA/CA |
|---|---|---|
| Prinzip | Kollision **erkennen** | Kollision **vermeiden** |
| Medium | Kupferkabel | Funk |
| Sender hört beim Senden? | Ja | Nein |
| Steuerpakete | Nein | Optional: RTS/CTS |

> **Merksatz:** Der MAC-Sublayer entscheidet, wer im Netzwerk reden darf – fair, effizient und möglichst ohne Zusammenstöße.

→ Siehe auch: [[Ethernet (IEEE 802.3)]] | [[WLAN (IEEE 802.11)]] | [[Sicherungsschicht]] | [[Kanalzuweisung]]
