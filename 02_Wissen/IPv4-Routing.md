### Grundlagen der Routingtabelle

Ein Router entscheidet anhand seiner **Routingtabelle**, wohin ein Paket weitergeleitet wird. Jede Zeile enthält:
- **Zielnetz**: Das Netzwerk, das erreicht werden soll.
- **Subnetzmaske**: Definiert die Größe des Zielnetzes.
- **Gateway / Next Hop**: Die IP-Adresse des nächsten Routers.
- **Schnittstelle (Interface)**: Der physikalische Ausgang am Router.
- **Metrik**: Kosten des Pfades (niedriger ist besser).

### Cisco-Konfiguration lesen

| Befehl / Begriff | Bedeutung |
|---|---|
| `hostname R1` | Name des Routers |
| `interface Ethernet0` | Konfiguration für den ersten LAN-Port |
| `ip address 10.0.0.1 255.255.255.0` | IP und Maske des Interfaces |
| `ip route [Ziel] [Maske] [Next-Hop]` | Statische Route einrichten |

**Beispiel:** `ip route 172.16.0.0 255.255.0.0 192.168.1.2`
- Zielnetz: `172.16.0.0/16`
- Erreichbar über den Nachbar-Router mit der IP `192.168.1.2`.

### Netzwerktopologie ermitteln

Aus einer Cisco-Konfig lässt sich die Umgebung ableiten:
1. **Direkt verbundene Netze**: Ergeben sich aus den `ip address` Einträgen der Interfaces.
2. **Entfernte Netze**: Ergeben sich aus den `ip route` Einträgen (diese liegen "hinter" dem Next Hop).

> **Merksatz:** Ein Router leitet Pakete nach dem "Longest Prefix Match"-Prinzip weiter – die spezifischste Route gewinnt.

→ Siehe auch: [[IPv4-Routing]] | [[OSI- und TCP-IP-Modell]] | [[Dijkstra-Algorithmus]]

## Lernkarten #Rechnernetze

Q: Was ist eine Routingtabelle und welche drei Kern-Informationen enthält ein Eintrag?
A: Eine Tabelle, die dem Router sagt, welcher Pfad zu welchem Netz führt. Kern-Infos: **Zielnetz** (inkl. Maske), **Metrik** (Kosten) und **Next Hop** (nächste Station).

Q: Wie lautet das Prinzip, nach dem Router die beste Route aus der Tabelle wählen?
A: **Longest Prefix Match** – es wird die Route gewählt, deren Subnetzmaske am genauesten (längsten) auf die Ziel-IP passt.

Q: Interpretiere: `ip route 10.1.0.0 255.255.0.0 192.168.0.2`
A: Pakete für das Netzwerk `10.1.0.0` (Maske `/16`) sollen an den Router mit der IP-Adresse `192.168.0.2` weitergeleitet werden.

Q: Woher kennt ein Router seine Routen?
A: 1. **Direkt verbunden** (über eigene Interfaces). 2. **Statische Routen** (manuell eingetragen). 3. **Dynamische Routen** (über Protokolle wie OSPF, BGP gelernt).
