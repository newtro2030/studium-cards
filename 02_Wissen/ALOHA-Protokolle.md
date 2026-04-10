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

## Lernkarten

Q: Was ist der maximale Durchsatz von Pure ALOHA?
A: **≈ 18,4 %** (1/(2e)), erreicht bei G = 0,5. Formel: S = G · e^(−2G).

Q: Was ist der maximale Durchsatz von Slotted ALOHA?
A: **≈ 36,8 %** (1/e), erreicht bei G = 1. Formel: S = G · e^(−G). Fast doppelt so effizient wie Pure ALOHA.

Q: Was ist der Unterschied zwischen Pure ALOHA und Slotted ALOHA?
A: **Pure ALOHA**: Senden jederzeit möglich → Kollisionen wenn Pakete sich ganz oder teilweise überlappen. **Slotted ALOHA**: Senden nur zu Beginn eines Zeitslots → Pakete können sich nur vollständig oder gar nicht überlappen → weniger Kollisionen.

Q: Welche modernen Protokolle basieren auf ALOHA-Prinzipien?
A: **CSMA/CD** (Ethernet – hört Medium vor dem Senden ab) und **CSMA/CA** (WLAN – vermeidet Kollisionen durch Wartezeit).
