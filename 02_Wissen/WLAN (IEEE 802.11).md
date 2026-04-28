### Grundlagen

- **Gemeinsames Medium:** Funkkanal (statt Kabel)
- **Zugriffsverfahren:** CSMA/CA (statt CSMA/CD)
- **Halbduplex:** Endgerät kann nicht gleichzeitig senden & empfangen

### Frequenzbänder

| Band | Nutzung |
|---|---|
| **2,4 GHz** | Weit verbreitet, aber störanfällig |
| **5 GHz** | Schneller, weniger überlaufen |
| **6 GHz** | Wi-Fi 6E, moderne Geräte |

### Architekturmodi

| Modus | Beschreibung |
|---|---|
| **Infrastrukturmodus** | Geräte kommunizieren über Access Point (AP) – Praxisstandard |
| **Ad-hoc-Modus** | Direkte Kommunikation zwischen Geräten, ohne AP |

**Begriffe:** STA = Station | AP = Access Point | BSS = Basic Service Set (1 AP + Geräte) | ESS = Extended Service Set (mehrere BSS mit Roaming)

### CSMA/CA & RTS/CTS

Funkgeräte können nicht gleichzeitig senden und hören → Kollisionen **nicht erkennbar** → Vermeidung nötig.

**RTS/CTS** gegen Hidden Node Problem:
1. STA sendet **RTS** an AP
2. AP antwortet mit **CTS**
3. Andere Stationen halten sich zurück

### Sicherheitsstandards

| Standard | Methode | Status |
|---|---|---|
| **WEP** | RC4-basiert | Veraltet, unsicher |
| **WPA** | TKIP + dynamische Schlüssel | Übergangslösung |
| **WPA2** | AES-CCMP | Derzeitiger Standard (seit 2004) |
| **WPA3** | SAE | Neuester Standard (seit 2018) |

### Wi-Fi-Generationen

| Standard | Datenrate | Frequenzband |
|---|---|---|
| 802.11b | 11 Mbit/s | 2,4 GHz |
| 802.11g | 54 Mbit/s | 2,4 GHz |
| 802.11n | bis 600 Mbit/s | 2,4 & 5 GHz |
| 802.11ac | bis 6,9 Gbit/s | 5 GHz |
| 802.11ax (Wi-Fi 6) | 9,6 Gbit/s | 2,4, 5, 6 GHz |

> **Merksatz:** WLAN ist Ethernet ohne Kabel – aber mit Funk, Kollisionsvermeidung und verschlüsseltem Zutritt.

→ Siehe auch: [[MAC-Sublayer]] | [[Drahtlose Übertragung]] | [[Ethernet (IEEE 802.3)]] | [[Kanalzuweisung]]

## Lernkarten #Rechnernetze

Q: Warum verwendet WLAN CSMA/CA statt CSMA/CD?
A: Funkgeräte können nicht gleichzeitig senden und empfangen → Kollisionen sind nicht erkennbar. Deshalb wird **Kollisionsvermeidung (CA)** statt Kollisionserkennung (CD) eingesetzt.

Q: Was ist das Hidden Node Problem und wie löst RTS/CTS es?
A: Zwei Stationen können sich nicht gegenseitig hören, aber der AP schon → Kollisionsgefahr. Lösung: Station sendet **RTS** → AP antwortet mit **CTS** → alle anderen Stationen halten sich zurück.

Q: Was ist der Unterschied zwischen Infrastrukturmodus und Ad-hoc-Modus?
A: **Infrastruktur**: Geräte kommunizieren über einen **Access Point** (Praxisstandard). **Ad-hoc**: Direkte Kommunikation zwischen Geräten ohne AP.

Q: Welche WLAN-Sicherheitsstandards gibt es in der richtigen Reihenfolge?
A: **WEP** (veraltet, unsicher) → **WPA** (Übergangslösung) → **WPA2** (AES-CCMP, aktueller Standard) → **WPA3** (seit 2018, stärkster Schutz).
