# Pufferungsebenen
#Rechnerarchitektur #Datenbanken #Speicher

Um die Auswirkungen der **Zugriffslücke** (Geschwindigkeitsunterschied zwischen CPU und Festplatte) zu minimieren, wird ein mehrstufiges Pufferungskonzept eingesetzt. Daten müssen auf ihrem Weg vom Datenträger zur CPU mehrere Ebenen durchlaufen.

## Die Ebenen im Überblick
Von der CPU hin zum physischen Datenträger:

1.  **CPU-Cache (L1, L2, L3):**
    - **Aufgabe:** Puffert Befehle und Daten direkt für den Prozessorkern.
    - **Verwaltung:** Durch die Hardware (CPU).
2.  **DBMS-Puffer (Datenbank-Puffer):**
    - **Aufgabe:** Hält häufig genutzte Datenbankblöcke im RAM, um teure Festplattenzugriffe zu vermeiden.
    - **Verwaltung:** Durch das Datenbank-Management-System (DBMS).
3.  **Dateisystem-Puffer (OS-Buffer / Page Cache):**
    - **Aufgabe:** Das Betriebssystem puffert Lese- und Schreibzugriffe auf Dateien im Hauptspeicher.
    - **Verwaltung:** Durch das Betriebssystem (OS).
4.  **Platten-Cache (Disk Cache):**
    - **Aufgabe:** Ein kleiner Speicher direkt auf der Festplatte/SSD, um Schreibvorgänge zu beschleunigen und Lesezugriffe vorzubereiten.
    - **Verwaltung:** Durch den Festplatten-Controller.
5.  **Datenträger:**
    - Die unterste Ebene (physische Speicherung, permanent).

## Verhalten und Besonderheiten
- **Schreibvorgänge:** Das "permanente Einbringen von Änderungen" ist kritisch. Ein DBMS muss oft sicherstellen, dass Daten wirklich auf der Ebene 5 (Datenträger) angekommen sind, bevor eine Transaktion als erfolgreich gilt (siehe WAL-Prinzip).
- **Lesezugriffe:** Jede Ebene versucht, die Anfrage zu beantworten. Erst wenn ein Datum in keiner Pufferebene gefunden wird, muss der physische Datenträger gelesen werden.

## Lernkarten #Rechnerarchitektur #Datenbanken

Q: Nenne die 4 typischen Pufferungsebenen zwischen CPU und Datenträger.
A: 1. CPU-Cache, 2. DBMS-Puffer, 3. Dateisystem-Puffer, 4. Platten-Cache.

Q: Warum ist das mehrstufige Pufferungskonzept besonders bei Datenbank-Schreibvorgängen kritisch?
A: Weil Daten in den oberen Puffern (RAM) flüchtig sind. Für die ACID-Eigenschaft "Dauerhaftigkeit" muss das DBMS sicherstellen, dass Änderungen durch alle Pufferstufen hindurch permanent auf den Datenträger geschrieben werden.

Q: Wer verwaltet den DBMS-Puffer und was ist sein Ziel?
A: Das Datenbank-Management-System selbst verwaltet diesen Puffer. Das Ziel ist es, die Anzahl der physischen Externspeicherzugriffe (I/O) zu minimieren, indem relevante Blöcke im RAM gehalten werden.
