# DHCP (Dynamic Host Configuration Protocol)

### Zweck
DHCP ermöglicht die automatische Zuweisung von IP-Adressen und weiteren Konfigurationsparametern (z. B. Subnetzmaske, Gateway, DNS-Server) an Geräte in einem Netzwerk.

### Der DORA-Prozess (Ablauf einer Sitzung)

Nach dem Bootvorgang läuft folgender 4-Schritte-Prozess zwischen Client und Server ab:

1.  **Discovery (Entdeckung)**:
    - Der Client schickt einen **DHCPDISCOVER** per Broadcast (`255.255.255.255`) ins Netz.
    - "Hallo, ich bin neu hier und brauche eine IP!"
2.  **Offer (Angebot)**:
    - Ein (oder mehrere) DHCP-Server antworten mit einem **DHCPOFFER**.
    - Enthält einen Adressvorschlag und die Konfigurationsdaten.
3.  **Request (Anforderung)**:
    - Der Client wählt ein Angebot aus und schickt einen **DHCPREQUEST** (wieder per Broadcast).
    - "Ich nehme das Angebot von Server X an!" (Teilt damit auch anderen Servern mit, dass er deren Angebot ablehnt).
4.  **Acknowledge (Bestätigung)**:
    - Der Server bestätigt die Zuweisung mit einem **DHCPACK**.
    - Erst jetzt darf der Client die IP-Adresse offiziell nutzen.

### Lease-Zeit
Die IP wird nicht dauerhaft vergeben, sondern nur für eine bestimmte Zeit (**Lease Time**). Der Client muss die Lease rechtzeitig verlängern (Renewal).

> **Merksatz:** D-O-R-A hilft dem Client auf die Sprünge, damit er im Netz die richtigen Daten kriege.

→ Siehe auch: [[OSI- und TCP-IP-Modell]] | [[IPv4-Routing]]

## Lernkarten

Q: Wofür steht DHCP und was ist seine Hauptaufgabe?
A: **Dynamic Host Configuration Protocol**. Automatische Zuweisung von IP-Adressen und Konfigurationsdaten (Gateway, DNS) an Netzwerkgeräte.

Q: Erläutere den DORA-Prozess kurz.
A: **D**iscovery (Suche), **O**ffer (Angebot des Servers), **R**equest (Anforderung durch Client), **A**cknowledge (Bestätigung durch Server).

Q: Warum werden DHCP-Discovery und Request als Broadcast gesendet?
A: **Discovery**: Weil der Client noch keine IP hat und nicht weiß, wo der Server ist. **Request**: Um dem gewählten Server die Annahme und allen anderen Servern die Ablehnung ihrer Angebote gleichzeitig mitzuteilen.

Q: Was passiert, wenn die Lease-Zeit einer IP-Adresse abläuft?
A: Der Client muss vor Ablauf der Zeit eine Verlängerung anfordern. Schlägt dies fehl, verliert er die IP-Adresse und muss den DORA-Prozess von vorn beginnen.
