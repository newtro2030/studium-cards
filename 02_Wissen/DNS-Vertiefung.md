# DNS-Vertiefung

### Zweck
Das **Domain Name System** übersetzt menschenlesbare Namen (z. B. `www.google.de`) in computerlesbare IP-Adressen (z. B. `142.250.185.67`).

### Resource Records (RR)

Datenbankeinträge im DNS. Wichtige Typen:

| Typ | Zweck |
|---|---|
| **A** | Host-Adresse: Verknüpft Hostnamen mit einer **IPv4**-Adresse. |
| **AAAA** | Host-Adresse: Verknüpft Hostnamen mit einer **IPv6**-Adresse. |
| **MX** | Mail Exchange: Gibt an, welcher Mailserver für die Domain zuständig ist. |
| **NS** | Name Server: Gibt den autoritativen DNS-Server für eine Zone an. |
| **CNAME** | Canonical Name: Ein Alias (Spitzname) für einen anderen Hostnamen. |
| **PTR** | Pointer: Rückwärtsauflösung (IP-Adresse → Name). |

### Ablauf der Namensauflösung (Beispiel `www.dhge.de`)

1.  **Anfrage vom Client**: Der Rechner fragt seinen lokalen DNS-Resolver (meist beim Provider).
2.  **Rekursion**: Wenn der Provider-Server die Antwort nicht kennt, fragt er hierarchisch weiter:
    - Fragt **Root-Server** (`.`): "Wer ist für `.de` zuständig?" → Verweis auf TLD-Server.
    - Fragt **TLD-Server** (`.de`): "Wer ist für `dhge.de` zuständig?" → Verweis auf den autoritativen Nameserver der DHGE.
    - Fragt **autoritativen Nameserver** (`dhge.de`): "Welche IP hat `www`?" → Antwortet mit der IP-Adresse (A-Record).
3.  **Caching**: Das Ergebnis wird auf dem Weg zurück zwischengespeichert, um zukünftige Anfragen zu beschleunigen.

> **Merksatz:** DNS ist das Telefonbuch des Internets – ohne Namen müsste man sich nur Zahlen merken.

→ Siehe auch: [[OSI- und TCP-IP-Modell]] | [[Netzwerkstandards]]

## Lernkarten

Q: Nenne 4 Typen von Resource Records (RR) im DNS und ihren Zweck.
A: 1. **A**: IPv4-Adresse zu Name. 2. **MX**: Mailserver-Zuweisung. 3. **NS**: Verantwortlicher Nameserver. 4. **CNAME**: Alias für einen anderen Namen.

Q: Erläutere an einem Beispiel die Auflösung eines FQDN (z. B. `www.test.de`).
A: Der Resolver fragt den **Root-Server** (`.`) → Verweis auf **TLD-Server** (`.de`) → Verweis auf **autoritativen Nameserver** der Domain (`test.de`) → Dieser liefert den **A-Record** für `www`.

Q: Was ist der Unterschied zwischen rekursiver und iterativer Namensauflösung?
A: **Rekursiv**: Der angefragte Server übernimmt die Arbeit und liefert die fertige IP. **Iterativ**: Der angefragte Server liefert nur einen Verweis auf den nächsten Server ("Ich weiß es nicht, aber frag mal den hier").

Q: Warum ist DNS im UDP-Protokoll (Port 53) realisiert?
A: Wegen der Geschwindigkeit und des geringen Overheads. Eine DNS-Anfrage ist meist klein und erfordert keinen aufwendigen Verbindungsaufbau wie bei TCP.
