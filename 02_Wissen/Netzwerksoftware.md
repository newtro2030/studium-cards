### Warum Schichtenarchitektur?

Netzwerksoftware wird in **Schichten (Layers)** organisiert, um:
- Komplexität zu reduzieren (funktionale Aufteilung)
- Jede Schicht erledigt spezifische Aufgaben und **nutzt Dienste der darunterliegenden Schicht**
- Änderungen in einer Schicht wirken sich **nicht direkt auf andere** aus (Isolation)

### Dienste, Schnittstellen, Protokolle

| Begriff | Bedeutung | Richtung |
|---|---|---|
| **Dienst (Service)** | Funktion, die eine Schicht der höheren anbietet | vertikal (im selben Gerät) |
| **Schnittstelle (Interface)** | Wie eine Schicht durch die darüberliegende angesprochen wird | vertikal |
| **Protokoll** | Regeln zwischen **gleichrangigen** Schichten auf verschiedenen Geräten | horizontal |

⚠️ **Protokolle = horizontal** (gleiche Schichten, verschiedene Geräte)
⚠️ **Dienste = vertikal** (zwischen Schichten im selben Gerät)

### Diensttypen

| Diensttyp | Beschreibung | Beispiel |
|---|---|---|
| **Verbindungsorientiert** | Aufbau → Nutzung → Abbau | Telefon, TCP |
| **Verbindungslos** | Jedes Paket separat, kein fester Pfad | IP, Postkarte |

Weitere Eigenschaften:
- Bestätigt oder **unbestätigt**
- Geordnet oder **ungeordnet**
- Zuverlässig oder **nicht zuverlässig**

### Was regelt ein Protokoll?

- Struktur der Nachrichten
- Reihenfolge
- Fehlerkorrektur
- Wiederholungen
- Datenflusssteuerung

→ Siehe auch: [[OSI- und TCP-IP-Modell]] | [[Rechnernetze – Überblick]]

## Lernkarten

Q: Was ist der Unterschied zwischen einem Dienst und einem Protokoll?
A: **Dienst**: Was eine Schicht der darüberliegenden anbietet (vertikal, im selben Gerät). **Protokoll**: Regeln zwischen gleichrangigen Schichten auf verschiedenen Geräten (horizontal).

Q: Warum wird Netzwerksoftware in Schichten organisiert?
A: Um Komplexität zu reduzieren: Jede Schicht erledigt spezifische Aufgaben, nutzt Dienste der darunter liegenden Schicht, und Änderungen in einer Schicht wirken sich nicht direkt auf andere aus.

Q: Was ist der Unterschied zwischen verbindungsorientierten und verbindungslosen Diensten?
A: **Verbindungsorientiert**: Aufbau → Nutzung → Abbau (z. B. TCP, Telefon). **Verbindungslos**: Jedes Paket separat, kein fester Pfad (z. B. IP, UDP).
