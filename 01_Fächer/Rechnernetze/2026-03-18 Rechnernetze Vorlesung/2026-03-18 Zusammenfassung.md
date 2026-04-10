# Rechnernetze Grundlagen – Zusammenfassung (Teil 1)

#Rechnernetze #Netzwerke #Klausurvorbereitung #Informatik #OSI #TCPIP #Grundlagen

---

## 1. Grundlagen von Rechnernetzen

### 1. Kerngedanken
Ein **Rechnernetz** ist die Gesamtheit aller Einrichtungen, die Kommunikation ermöglichen:

- Übertragungswege (Kupfer, Glasfaser, Funk)
- Übertragungseinrichtungen (z. B. Repeater)
- Vermittlungs-/Verteilungseinrichtungen
- Endgeräte

👉 Ziel: **Bereitstellung von Diensten**

👉 Wichtig: Es gibt **keine einheitliche Klassifikation** von Netzwerken.

---

### 2. Wichtige Begriffe

- **Verteilung (Broadcast)**  
  → Nachricht an alle Teilnehmer  

- **Vermittlung (Switching)**  
  → gezielte Verbindung zwischen Teilnehmern  

- **Point-to-Point**  
  → 1 Sender ↔ 1 Empfänger  

- **Broadcast**  
  → 1 Sender → viele Empfänger  

- **Simplex / Halbduplex / Vollduplex**
  - Simplex: eine Richtung  
  - Halbduplex: abwechselnd  
  - Vollduplex: gleichzeitig  

- **Verbindungsorientiert**
  → feste Verbindung (z. B. Telefon)

- **Verbindungslos**
  → einzelne Pakete (z. B. Internet/IP)

---

### 3. Zusammenhänge verstehen

#### Verteilung vs. Vermittlung
- **Verteilung** = alle bekommen die Nachricht  
- **Vermittlung** = gezielte Kommunikation  

**Beispiele:**
- Radio → Verteilung  
- Telefon → Vermittlung  

👉 WLAN ist physikalisch **Broadcast**, wirkt aber logisch wie Punkt-zu-Punkt.

---

#### Verbindungsorientiert vs. Verbindungslos
- Verbindungsorientiert:
  - Reihenfolge garantiert
  - zuverlässig  

- Verbindungslos:
  - keine Garantie
  - Pakete können **1-3-2** ankommen  

👉 Internet (IP) ist **verbindungslos**, TCP macht es zuverlässig.

---

#### Store-and-Forward vs. Cut-Through

| Verfahren | Eigenschaften |
|----------|-------------|
| Store-and-Forward | komplett empfangen → dann senden |
| Cut-Through | sofort weiterleiten |

👉 Trade-off:
- Store-and-Forward = sicher  
- Cut-Through = schnell  

---

### 4. Typische Klausurfragen

**Unterschied Verteilung vs. Vermittlung?**  
→ Verteilung: an alle  
→ Vermittlung: gezielt  

**Warum kommt Reihenfolge durcheinander?**  
→ Verbindungslos (IP), unterschiedliche Wege  

**Warum nicht immer Cut-Through?**  
→ keine Fehlerprüfung  

**Ist WLAN Broadcast oder Point-to-Point?**  
→ physikalisch Broadcast  

---

### 5. Häufige Fehler

- ❌ Internet ist verbindungsorientiert  
- ❌ Broadcast wird kaum genutzt  
- ❌ Reihenfolge ist immer korrekt  

---

## 2. Netzwerkarten und Klassifikation

### 1. Kerngedanken
Netze werden klassifiziert nach:
- Größe
- Technologie
- Zweck

---

### 2. Wichtige Begriffe

- **PAN** → ~1 m (Bluetooth)  
- **LAN** → Gebäude / Firma  
- **MAN** → Stadt  
- **WAN** → global  

- **Inter-Network**
  → Zusammenschluss mehrerer Netze  

- **Gateway**
  → verbindet unterschiedliche Netze  

---

### 3. Zusammenhänge verstehen

#### Internet = Netzwerk von Netzwerken
- viele unterschiedliche Netze
- verbunden über Router/Gateways  

👉 Internet = **Inter-Network**

---

#### LAN vs. WAN

| LAN | WAN |
|-----|-----|
| lokal | global |
| hohe Datenrate | heterogen |
| kontrolliert | komplex |

---

#### VPN
- virtuelles Netz über Internet  

**Vorteile:**
- flexibel
- skalierbar  

**Nachteile:**
- keine garantierte Leistung  

---

### 4. Typische Klausurfragen

**Unterschied LAN vs. WAN?**  
→ LAN lokal, WAN global  

**Was ist ein Inter-Network?**  
→ Netz aus mehreren Netzen  

**Aufgabe Gateway?**  
→ Verbindung inkompatibler Netze  

---

### 5. Häufige Fehler

- ❌ Internet = WAN  
- ❌ VPN ist ein eigenes physisches Netz  

---

## 3. Client-Server vs. Peer-to-Peer

### 1. Kerngedanken
Zwei Modelle:
- Client-Server
- Peer-to-Peer

---

### 2. Wichtige Begriffe

- **Client**
  → fordert Dienst an  

- **Server**
  → bietet Dienst  

- **Peer-to-Peer**
  → keine festen Rollen  

---

### 3. Zusammenhänge verstehen

#### Client-Server
- zentral
- kontrollierbar  

Beispiel: Web

---

#### Peer-to-Peer
- dezentral
- skalierbar  

Beispiel: Filesharing  

---

👉 Vergleich:

| Kriterium | Client-Server | P2P |
|----------|--------------|-----|
| Kontrolle | hoch | gering |
| Skalierung | begrenzt | gut |
| Ausfallrisiko | hoch | gering |

---

### 4. Typische Klausurfragen

**Vorteil P2P?**  
→ Skalierbarkeit  

**Nachteil Client-Server?**  
→ Single Point of Failure  

---

### 5. Häufige Fehler

- ❌ P2P hat keine Struktur  

---

## 4. Übertragungsarten & Grundlagen

### 1. Kerngedanken
Übertragung:
- geführt (Kabel)
- ungeführt (Funk)

---

### 2. Wichtige Begriffe

- **Geführt**
  → Kupfer, Glasfaser  

- **Ungeführt**
  → Funk, Infrarot  

- **Bandbreite**
  - physikalisch: Hz  
  - informatisch: bit/s  

---

### 3. Zusammenhänge verstehen

#### Bandbreite vs. Datenrate
- Bandbreite (Hz) bestimmt mögliche Datenrate  

👉 Mehr Frequenzen → mehr Daten

---

#### Bitrate vs. Baudrate
- **Baudrate** = Symbole/s  
- **Bitrate** = Bits/s  

👉 1 Symbol kann mehrere Bits enthalten

---

### 4. Typische Klausurfragen

**Bitrate vs. Baudrate?**  
→ Symbole vs. Bits  

**Warum begrenzt Bandbreite die Datenrate?**  
→ weniger Frequenzen → weniger Information  

---

### 5. Häufige Fehler

- ❌ Bitrate = Baudrate  
- ❌ Bandbreite ist immer bit/s  

---

## 🧠 Lernanker (für schnelle Wiederholung)

- Internet = **verbindungslos (IP)**
- TCP = macht es **zuverlässig**
- WLAN = **Broadcast**
- Cut-Through = **schnell, unsicher**
- Store-and-Forward = **langsam, sicher**
- Bitrate ≠ Baudrate
- Bandbreite (Hz) ≠ Datenrate (bit/s)

---

## 📌 Tags für Obsidian

#Broadcast #Vermittlung #TCP #IP #LAN #WAN #VPN #ClientServer #PeerToPeer #Bitrate #Baudrate #Bandbreite #Netzwerkgrundlagen