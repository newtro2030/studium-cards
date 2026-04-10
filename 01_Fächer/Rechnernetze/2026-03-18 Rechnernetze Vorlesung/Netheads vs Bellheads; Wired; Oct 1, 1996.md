Artikel: https://www.wired.com/1996/10/atm-3/
## 🧠 Kernaussage
Der Artikel beschreibt den Konflikt zwischen zwei Netzwerk-Philosophien:
- **ATM (Asynchronous Transfer Mode)** → komplex, geplant, kontrolliert  
- **Internet (TCP/IP)** → einfach, dezentral, robust  

👉 Zentrale These:
> Ein einfaches, skalierbares System setzt sich gegen ein komplexes, perfektes System durch.

---

## ⚙️ ATM (Asynchronous Transfer Mode)

### Eigenschaften
- Feste Zellgröße: **53 Byte**
- Verbindungsorientiert
- Garantierte **Quality of Service (QoS)**
- Geeignet für:
  - Sprache
  - Video
  - Daten

### Ziel
Ein einheitliches Netzwerk für alle Kommunikationsarten („One Network for Everything“)

### Vorteile
- Planbare Performance
- Garantierte Bandbreite
- Geringe Latenz (theoretisch)

### Nachteile
- Sehr **komplex**
- Hohe Kosten
- Schwer skalierbar
- Unflexibel bei unvorhersehbarem Traffic

---

## 🌐 Internet (TCP/IP)

### Eigenschaften
- Paketbasiert (variable Größe)
- **Best-Effort-Prinzip** (keine Garantie)
- Dezentral organisiert
- Fehlerbehandlung auf höheren Schichten (z. B. TCP)

### Vorteile
- Einfach
- Robust
- Sehr gut skalierbar
- Kostengünstig

### Nachteile
- Keine garantierte Qualität (QoS)
- Potenziell unzuverlässiger

---

## ⚔️ Der Konflikt: Bellheads vs Netheads

### Bellheads (ATM-Welt)
- Telekommunikationsindustrie
- Zentralisierte Planung
- Fokus auf Kontrolle & Qualität

### Netheads (Internet-Welt)
- Internet-Community
- Dezentrale Architektur
- Fokus auf Wachstum & Pragmatismus

---

## 🔍 Zentrale Kritik an ATM
- Reale Netzwerke sind **nicht planbar**
- Traffic ist **burstartig** (unregelmäßig)
- Komplexe Steuerung funktioniert in der Praxis schlecht
- Hoher Implementierungsaufwand

---

## 💡 Erfolgsprinzip des Internets
- „Dumme“ Infrastruktur + „intelligente“ Endsysteme
- Fehler werden oben korrigiert (End-to-End-Prinzip)
- Wachstum wichtiger als Perfektion

---

## 📉 Implizite Prognose (1996)
ATM wirkt technisch überlegen, aber:
- Internet wird sich durchsetzen wegen:
  - Einfachheit
  - Kosten
  - Skalierbarkeit

👉 Rückblick: Prognose war korrekt

---

## 🧩 Fazit
> Komplexe Systeme scheitern oft an der Realität.  
> Einfache Systeme gewinnen durch Skalierbarkeit.

---

## 🔗 Verwandte Themen
- [[OSI-Modell]]
- [[TCP/IP]]
- [[QoS]]
- [[End-to-End-Prinzip]]
- [[Netzwerkarchitekturen]]

---

## 🏷️ Tags
#Rechnernetze #ATM #TCPIP #Internet #QoS #Architektur #Geschichte