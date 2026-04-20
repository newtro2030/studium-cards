# Transaktionskonzept & ACID
#Datenbanken #Transaktionen

Transaktionen sind Update-Operationen (im Sinne der Datenbanktechnologie), die eine logisch abgeschlossene Arbeitseinheit bilden. Sie überführen die Datenbank von einem konsistenten Zustand in einen neuen konsistenten Zustand.

## ACID-Eigenschaften
Jede Transaktion muss die ACID-Eigenschaften erfüllen:

1.  **Atomarität (Atomicity):** „Alles-oder-nichts-Prinzip“. Eine Transaktion wird entweder ganz oder gar nicht ausgeführt.
2.  **Konsistenz (Consistency):** Eine Transaktion hinterlässt die Datenbank in einem konsistenten (gültigen) Zustand. Während der Ausführung kann die Konsistenz kurzzeitig verletzt sein.
3.  **Isolation (Isolation):** Nebenläufige Transaktionen dürfen sich nicht gegenseitig beeinflussen. Jede Transaktion hat das Gefühl, alleine auf der Datenbank zu arbeiten.
4.  **Dauerhaftigkeit (Durability):** Nach einem erfolgreichen Abschluss (`COMMIT`) bleiben die Änderungen permanent in der Datenbank gespeichert, auch bei einem Systemausfall.

---

## Synchronisationsverfahren
Um die Isolation sicherzustellen, gibt es verschiedene Ansätze:

### Pessimistische Synchronisation (Sperrverfahren)
- Objekte werden vor dem Zugriff gesperrt (**Locking**).
- **2-Phasen-Sperrprotokoll (2PL):**
    - **Wachstumsphase:** Sperren werden angefordert, keine freigegeben.
    - **Schrumpfungsphase:** Sperren werden freigegeben (am Transaktionsende), keine neuen angefordert.
- **RX-Sperrverfahren:** Unterscheidung zwischen Read (Shared) und eXclusive (Write) Sperren.

### Optimistische Synchronisation
Geht davon aus, dass Konflikte selten sind. Keine Sperren während der Bearbeitung.
1.  **Lesephase:** Verarbeitung findet im Puffer statt.
2.  **Validierungsphase:** Beim Abschluss wird geprüft, ob Konflikte mit anderen Transaktionen aufgetreten sind. Falls ja -> Rollback.
3.  **Schreibphase:** Wenn keine Konflikte -> Änderungen permanent machen und Log-Einträge schreiben.

## Lernkarten #Datenbanken

Q: Was ist eine Transaktion im Datenbankkontext?
A: Eine logisch zusammengehörige Folge von Datenbankoperationen, die als eine Einheit betrachtet wird (z. B. eine Banküberweisung).

Q: Erkläre die Isolationseigenschaft (ACID).
A: Isolation bedeutet, dass gleichzeitig ablaufende Transaktionen so ausgeführt werden müssen, als ob sie nacheinander (seriell) ablaufen würden. Zwischenzustände einer Transaktion sind für andere nicht sichtbar.

Q: Was ist der Hauptunterschied zwischen pessimistischer und optimistischer Synchronisation?
A: 
- **Pessimistisch:** Verhindert Konflikte durch Sperren (Locks) vorab.
- **Optimistisch:** Erlaubt parallele Bearbeitung ohne Sperren und prüft erst am Ende (Validierung), ob ein Konflikt entstanden ist.
