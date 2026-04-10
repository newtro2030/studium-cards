### OSI-Modell (7 Schichten)

Konzeptionelles, theoretisches Modell der ISO zur Standardisierung von Netzwerkkommunikation.

| Nr. | Schicht | Aufgabe |
|---|---|---|
| 7 | **Anwendung** (Application) | Dienste für Benutzeranwendungen (E-Mail, Web, FTP) |
| 6 | **Darstellung** (Presentation) | Datenformate, Verschlüsselung, Komprimierung |
| 5 | **Sitzung** (Session) | Aufbau, Steuerung, Beendigung von Sitzungen |
| 4 | **Transport** | Zuverlässiger Transport, Flusskontrolle (TCP) |
| 3 | **Vermittlung** (Network) | Routing, logische Adressen (IP), Fragmentierung |
| 2 | **Sicherung** (Data Link) | Rahmenbildung, Fehlererkennung, MAC-Adressen |
| 1 | **Bitübertragung** (Physical) | Elektrische/optische Signalübertragung, Kabel |

**Merkhilfe:** „Alle Deutschen Studenten Trinken Verschiedene Sorten Bier" (7→1)

**Vorteile:** Klare Trennung, Modularität, Standardisierung
**Nachteile:** Komplex, kam zu spät, politisch überholt von TCP/IP

### TCP/IP-Modell (4 Schichten)

Praxisorientiertes Modell, de-facto Standard des Internets (aus ARPANET).

| Nr. | Name | Entspricht OSI | Protokolle |
|---|---|---|---|
| 4 | **Anwendung** | Schichten 5–7 | HTTP, SMTP, DNS, FTP |
| 3 | **Transport** | Schicht 4 | TCP (zuverlässig), UDP (schnell) |
| 2 | **Internet** | Schicht 3 | IP, Routing, ICMP |
| 1 | **Netzwerkzugriff** | Schichten 1–2 | Ethernet, WLAN, ARP |

**Vorteile:** Einfacher, praxisorientiert, Basis des Internets
**Nachteile:** Weniger klare Trennung, keine eigenen Schichten für Darstellung/Sitzung

### Vergleich OSI vs. TCP/IP

| Merkmal | OSI-Modell | TCP/IP-Modell |
|---|---|---|
| Anzahl Schichten | 7 | 4–5 |
| Praxisrelevanz | Theoretisch wichtig | Praktisch weltweit genutzt |
| Ursprung | ISO-Norm | ARPANET |
| Modularität | Sehr strikt | Flexibler, aber unsauber |
| Sitzungs-/Darstellungsschicht | Ja | Nein (Teil der Anwendung) |

> **Merksatz:** Das OSI-Modell erklärt, wie Netzwerke funktionieren *sollten* – TCP/IP zeigt, wie sie *wirklich* funktionieren.

→ Siehe auch: [[Netzwerksoftware]] | [[Sicherungsschicht]] | [[Ethernet (IEEE 802.3)]]

## Lernkarten

Q: Nenne die 7 Schichten des OSI-Modells (von oben nach unten).
A: 7 Anwendung, 6 Darstellung, 5 Sitzung, 4 Transport, 3 Vermittlung, 2 Sicherung, 1 Bitübertragung. **Merkhilfe**: „Alle Deutschen Studenten Trinken Verschiedene Sorten Bier"

Q: Welche 4 Schichten hat das TCP/IP-Modell?
A: 4 **Anwendung** (HTTP, DNS, SMTP), 3 **Transport** (TCP, UDP), 2 **Internet** (IP, ICMP), 1 **Netzwerkzugriff** (Ethernet, WLAN, ARP).

Q: Welche OSI-Schichten sind in der TCP/IP-Anwendungsschicht zusammengefasst?
A: Die OSI-Schichten 5 (Sitzung), 6 (Darstellung) und 7 (Anwendung).

Q: Was ist der Hauptunterschied zwischen OSI- und TCP/IP-Modell?
A: OSI ist ein theoretisches Referenzmodell (7 Schichten, strikt modular). TCP/IP ist praxisorientiert (4 Schichten), de-facto Standard des Internets – aus dem ARPANET entstanden.
