### Definition

> Ein **Rechnernetz** ist die Gesamtheit aller Einrichtungen, die Kommunikation ermöglichen: Übertragungswege, Übertragungseinrichtungen, Vermittlungseinrichtungen und Endgeräte.

**Ziel:** Bereitstellung von Diensten

### Teilgebiete

```
Rechnernetze
├── Kapitel 1 – Grundlagen
│   ├── [[Netzwerktypen (PAN, LAN, MAN, WAN)]]
│   ├── [[Netzwerksoftware]]
│   ├── [[OSI- und TCP-IP-Modell]]
│   └── [[Netzwerkstandards]]
├── Kapitel 2 – Physical Layer
│   ├── [[Physikalische Datenübertragung]]
│   ├── [[Übertragungsmedien]]
│   ├── [[Drahtlose Übertragung]]
│   ├── [[PSTN]]
│   ├── [[Mobilfunk]]
│   └── [[Kabelfernsehnetze]]
└── Kapitel 3/4 – Data Link & MAC Layer
    ├── [[Sicherungsschicht]]
    ├── [[Framing]]
    ├── [[Fehlererkennung]]
    ├── [[Fehlerkorrektur]]
    ├── [[Flusskontrolle]]
    ├── [[MAC-Sublayer]]
    ├── [[Ethernet (IEEE 802.3)]]
    ├── [[WLAN (IEEE 802.11)]]
    ├── [[Kanalzuweisung]]
    └── [[ALOHA-Protokolle]]
```

### Kommunikationsarten

| Begriff | Bedeutung |
|---|---|
| **Simplex** | Nur eine Richtung (z. B. Radio) |
| **Halbduplex** | Abwechselnd (z. B. Walkie-Talkie) |
| **Vollduplex** | Gleichzeitig (z. B. Telefon) |
| **Point-to-Point** | 1 Sender ↔ 1 Empfänger |
| **Broadcast** | 1 Sender → viele Empfänger |

### Vermittlung vs. Verteilung

| Begriff | Bedeutung |
|---|---|
| **Verteilung (Broadcast)** | Nachricht geht an alle |
| **Vermittlung (Switching)** | Gezielte Verbindung zwischen Teilnehmern |

⚠️ WLAN ist **physikalisch Broadcast**, verhält sich logisch wie Point-to-Point.

### Verbindungsorientiert vs. Verbindungslos

| Typ | Eigenschaft | Beispiel |
|---|---|---|
| **Verbindungsorientiert** | Feste Verbindung, Reihenfolge garantiert | Telefon |
| **Verbindungslos** | Jedes Paket separat, Reihenfolge nicht garantiert | Internet (IP) |

⚠️ Das **Internet (IP) ist verbindungslos** – TCP macht es zuverlässig.

### Store-and-Forward vs. Cut-Through

| Verfahren | Eigenschaft |
|---|---|
| **Store-and-Forward** | Komplett empfangen → dann weiterleiten. Sicher, langsam. |
| **Cut-Through** | Sofort weiterleiten. Schnell, keine Fehlerprüfung. |

### Netzwerkarchitekturen

| Modell | Merkmale |
|---|---|
| **Client-Server** | Zentral, kontrollierbar, Single Point of Failure |
| **Peer-to-Peer (P2P)** | Dezentral, skalierbar, robuster |

→ Siehe auch: [[Netzwerktypen (PAN, LAN, MAN, WAN)]] | [[OSI- und TCP-IP-Modell]] | [[Netzwerkstandards]]
