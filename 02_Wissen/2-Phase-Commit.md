# 2-Phasen-Commit-Protokoll (2PC)
#Datenbanken #Transaktionen #Verteilt

Wenn Transaktionen auf mehreren Verarbeitungsknoten (verteilte Datenbanken) ausgeführt werden, muss die **Atomarität** über alle Knoten hinweg sichergestellt werden. Dies geschieht durch das **2-Phasen-Commit-Protokoll**.

## Ablauf
Der Prozess wird von einem **Koordinator** gesteuert, der mit mehreren **Agenten** (beteiligte Knoten) kommuniziert.

### 1. Vorbereitungsphase (Prepare Phase)
1. Der Koordinator sendet eine `PREPARE`-Anforderung an alle Agenten.
2. Jeder Agent führt seine Teiltransaktion bis zum Ende aus, sichert seine Log-Daten auf stabilen Speicher und schreibt einen `PREPARED`-Satz ins Log.
3. Die Agenten antworten dem Koordinator mit `READY` (erfolgreich vorbereitet) oder `FAILED` (Fehler, lokaler Rollback).

### 2. Entscheidungsphase (Commit/Rollback Phase)
- **Commit:** Wenn **alle** Agenten `READY` gemeldet haben:
  1. Koordinator schreibt `COMMIT` in sein Log.
  2. Koordinator sendet `COMMIT` an alle Agenten.
  3. Agenten schreiben `COMMIT` ins Log und schließen die Transaktion ab.
- **Rollback:** Wenn **mindestens ein** Agent `FAILED` gemeldet hat (oder ein Timeout auftritt):
  1. Koordinator schreibt `ROLLBACK` in sein Log.
  2. Koordinator sendet `ROLLBACK` an alle Agenten.
  3. Agenten machen ihre Änderungen rückgängig (`UNDO`) und schreiben `ROLLBACK` ins Log.

### Abschluss
Die Agenten senden eine Bestätigung (`ACK`) an den Koordinator. Sobald alle `ACK` eingegangen sind, ist die Transaktion für den Koordinator beendet.

## Lernkarten #Datenbanken

Q: Was ist das Ziel des 2-Phasen-Commit-Protokolls?
A: Die Sicherstellung der Atomarität bei verteilten Transaktionen. Es stellt sicher, dass entweder alle beteiligten Knoten die Änderungen übernehmen (Commit) oder keiner (Rollback).

Q: Was passiert im 2PC, wenn ein Agent mit "FAILED" antwortet?
A: Der Koordinator bricht die gesamte Transaktion ab und sendet einen ROLLBACK-Befehl an alle anderen beteiligten Agenten, damit die Konsistenz gewahrt bleibt.

Q: Welche zwei Phasen gibt es beim 2PC?
A: 
1. **Vorbereitungsphase (Prepare):** Agenten bereiten Commit vor und melden Bereitschaft.
2. **Entscheidungsphase (Commit/Rollback):** Koordinator trifft finale Entscheidung basierend auf den Rückmeldungen.
