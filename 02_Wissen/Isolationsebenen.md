# Isolationsebenen (SQL92)
#Datenbanken #Transaktionen #Isolation

Isolationsebenen definieren, inwieweit eine Transaktion von Änderungen anderer, parallel laufender Transaktionen abgeschirmt wird. Je höher die Isolation, desto geringer die Performance (durch Sperren).

## Phänomene bei ungenügender Isolation
- **Dirty Read:** Eine Transaktion liest Daten, die von einer anderen Transaktion geändert, aber noch nicht festgeschrieben (`COMMIT`) wurden.
- **Non-Repeatable Read:** Zweimaliges Lesen desselben Datensatzes liefert unterschiedliche Werte, da eine andere Transaktion dazwischen ein `UPDATE` gemacht hat.
- **Phantom Read:** Eine Suchabfrage (z. B. `SELECT COUNT(*)`) liefert unterschiedliche Ergebnismengen, da eine andere Transaktion Datensätze eingefügt (`INSERT`) oder gelöscht (`DELETE`) hat.

## Die Isolationsebenen
Basierend auf dem SQL92-Standard:

| Isolationsebene | Dirty Read | Non-Repeatable Read | Phantom Read |
| :--- | :---: | :---: | :---: |
| **READ UNCOMMITTED** | Möglich | Möglich | Möglich |
| **READ COMMITTED** | Ausgeschlossen | Möglich | Möglich |
| **REPEATABLE READ** | Ausgeschlossen | Ausgeschlossen | Möglich |
| **SERIALIZABLE** | Ausgeschlossen | Ausgeschlossen | Ausgeschlossen |

### Erläuterung
- **READ UNCOMMITTED:** Geringste Restriktion. Keine Sperren.
- **READ COMMITTED:** Standard in vielen DBMS (z.B. Oracle). Verhindert Dirty Reads.
- **REPEATABLE READ:** Sperrt gelesene Datensätze bis zum Transaktionsende.
- **SERIALIZABLE:** Höchste Stufe. Bereichssperren auf der Treffermenge verhindern auch das Einfügen neuer Datensätze (Phantome).

## Lernkarten #Datenbanken

Q: Was ist ein Dirty Read?
A: Wenn eine Transaktion Daten liest, die eine andere Transaktion zwar schon geändert, aber noch nicht mit COMMIT bestätigt hat. Wird die andere Transaktion später zurückgerollt, hat die erste Transaktion mit ungültigen Daten gearbeitet.

Q: Welche Isolationsebene verhindert alle drei negativen Phänomene (Dirty Read, Non-Repeatable Read, Phantom Read)?
A: **SERIALIZABLE**.

Q: Was ist der Unterschied zwischen Non-Repeatable Read und Phantom Read?
A: 
- **Non-Repeatable Read:** Ein existierender Datensatz ändert seinen **Inhalt** (Update).
- **Phantom Read:** Die **Anzahl** der Datensätze in einer Ergebnismenge ändert sich durch Einfügen oder Löschen (Insert/Delete).
