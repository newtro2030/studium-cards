#Datenbanken #Recovery

Die Überführung der Datenbank in einen konsistenten Zustand durch Fehlerbehebung nach einem Ausfall wird als **Recovery** oder **Wiederherstellung** bezeichnet.

## Recovery-Arten
Es werden zwei grundlegende Arten von Recovery-Operationen unterschieden:
- **Vorwärts-Recovery (rollforward):** Die Datenbank wird in einen (relativ zum Ausgangspunkt) neuen konsistenten Zustand überführt. Dabei werden Log-Dateien verarbeitet und Änderungen erneut ausgeführt (REDO).
- **Rückwärts-Recovery (rollback):** Die Datenbank wird in einen alten konsistenten Zustand versetzt. Dabei werden Änderungen rückgängig gemacht (UNDO).

## Fehlerarten (Failure Types)
Recovery-Verfahren müssen verschiedene Arten von Fehlern behandeln:
1. **Transaktionsfehler:** Eine einzelne Transaktion bricht ab (z. B. durch Division durch Null oder Benutzerabbruch). Lösung: Lokales Rollback (`UNDO`).
2. **Systemfehler (Soft Crash):** Systemabsturz oder Stromausfall. Der Inhalt des RAM (Datenbankpuffer) geht verloren, die Festplatte bleibt intakt. Lösung: `REDO` von abgeschlossenen und `UNDO` von nicht abgeschlossenen Transaktionen.
3. **Medienfehler (Hard Crash):** Defekt des Datenträgers (z. B. Headcrash). Teile der Datenbank auf Disk sind unlesbar. Lösung: Einspielen des letzten Backups (Sicherung) und anschließendes `REDO` aller Transaktionen aus den gesicherten Log-Archiven.

## Logging (Protokollierung)
Grundvoraussetzung für Recovery sind Aufzeichnungen über Datenbankinhalte und Änderungen im **Datenbank-Protokoll (Log)**.

### Protokollierungsformen
- **Physisches Logging (Zustands-logging):** Aufzeichnung von Seiteninhalten (Before-Image / After-Image).
- **Logisches Logging (Übergangs-logging):** Aufzeichnung der ausgeführten Operationen (z. B. "Erhöhe Kontostand um 100").
- **Physiologisches Logging:** Kombination aus beiden (Einträge beziehen sich auf Seiten, beschreiben aber Änderungen innerhalb der Seite logisch).

### Log-Einträge (Log Records)
Ein Log-Eintrag besteht meist aus:
- **LSN (Log Sequence Number):** Eindeutige Nummer des Eintrags.
- **Transaktions-ID:** Zuordnung zur verursachenden Transaktion.
- **Typ:** (Beginn, Commit, Rollback, Checkpoint, Update).
- **Undo Image:** Alter Inhalt (für Rollback).
- **Redo Image:** Neuer Inhalt (für Rollforward).

**Zusammenhang Operationen:**
- **INSERT:** Erfordert Redo-Image.
- **UPDATE:** Erfordert Undo- und Redo-Image.
- **DELETE:** Erfordert Undo-Image.

## Checkpoints (Sicherungspunkte)
Bei einem Checkpoint werden geänderte Datenblöcke aus dem Datenbankpuffer (RAM) auf die Datenträger (Disk) geschrieben.
- Sie dienen als **Aufsetzpunkte** für die Wiederherstellung.
- Reduzieren die Menge der beim Recovery zu verarbeitenden Log-Daten.

## Spezielle Begriffe
- **Write-Ahead Logging (WAL):** Log-Einträge müssen zwingend *vor* den eigentlichen Datenänderungen auf den stabilen Speicher geschrieben werden.
- **Compensation Log Record (CLR):** Ein spezieller Log-Satz, der das Rücksetzen (Undo) einer Operation selbst wieder protokolliert.

## Lernkarten #Datenbanken

Q: Was ist der Unterschied zwischen Vorwärts- und Rückwärts-Recovery?
A: 
- **Vorwärts-Recovery (Rollforward):** Nutzt REDO-Informationen, um Änderungen nach einem Systemabsturz erneut anzuwenden und einen aktuellen konsistenten Zustand zu erreichen.
- **Rückwärts-Recovery (Rollback):** Nutzt UNDO-Informationen, um nicht abgeschlossene Transaktionen rückgängig zu machen.

Q: Was ist die Aufgabe von Checkpoints im Recovery-Prozess?
A: Checkpoints minimieren den Recovery-Aufwand, indem sie sicherstellen, dass alle Änderungen bis zu diesem Zeitpunkt permanent auf Disk gespeichert sind. Das Recovery muss dann erst ab dem letzten Checkpoint beginnen.

Q: Welche Informationen enthält ein typischer Log-Eintrag?
A: LSN (Log Sequence Number), Transaktions-ID, Typ des Eintrags (z.B. Update), betroffener Datenblock/Datensatz, sowie Undo- und Redo-Images.

Q: Was besagt das Write-Ahead-Logging (WAL) Prinzip?
A: Dass Protokolleinträge (Log Records), die eine Änderung beschreiben, immer **zuerst** auf den stabilen Speicher geschrieben werden müssen, bevor die eigentliche Änderung in der Datenbank auf Disk permanent gemacht wird.
