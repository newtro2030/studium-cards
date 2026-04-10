### Ursprung

Entwickelt in den 1970ern an der **University of Hawaii** für drahtlose Funknetzwerke zwischen Inseln. Eines der ersten MAC-Protokolle für gemeinsam genutzte Medien.

### Pure ALOHA

- Jeder Host darf **jederzeit** ein Paket senden
- Keine Zeitfenster, keine Koordination
- Kein ACK → Kollision erkannt → zufällige Wartezeit → erneut senden
- Kollisionen wenn sich Pakete **ganz oder teilweise** überlappen

**Durchsatz:**
```
S = G · e^(-2G)    →    S_max = 1/(2e) ≈ 18,4%  (bei G = 0,5)
```

### Slotted ALOHA

- Zeit in **diskrete Slots** unterteilt (je ein Paket lang)
- Senden nur zu **Beginn eines Slots** erlaubt
- Pakete überlappen sich nur vollständig oder gar nicht → weniger Kollisionen

**Durchsatz:**
```
S = G · e^(-G)    →    S_max = 1/e ≈ 36,8%  (bei G = 1)
```

Fast **doppelt so effizient** wie Pure ALOHA.

### Vergleich

| Verfahren | Max. Durchsatz | Kollisionsfenster |
|---|---|---|
| **Pure ALOHA** | ≈ 18,4 % | 2 Paketlängen |
| **Slotted ALOHA** | ≈ 36,8 % | 1 Paketlänge |

### Nachfolger

ALOHA ist die theoretische Basis moderner Protokolle:
- **CSMA/CD** – hört Medium vor dem Senden ab (Ethernet)
- **CSMA/CA** – vermeidet Kollisionen durch Wartezeit (WLAN)

> **Merksatz:** ALOHA sagt: Sende, wenn du willst – aber rechne mit Chaos.

→ Siehe auch: [[Kanalzuweisung]] | [[MAC-Sublayer]] | [[Ethernet (IEEE 802.3)]] | [[WLAN (IEEE 802.11)]]
