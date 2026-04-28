# Zentraleinheit (CPU - Central Processing Unit)
#Rechnerarchitektur #CPU

Die CPU ist das "Gehirn" des Computers und führt die Anweisungen von Computerprogrammen aus. Nach der **Von-Neumann-Architektur** besteht die CPU im Kern aus drei Hauptkomponenten.

## Aufbau der CPU

### 1. Rechenwerk (ALU - Arithmetic Logic Unit)
Das Rechenwerk führt alle elementaren Operationen durch:
- **Arithmetische Operationen:** Addition, Subtraktion, etc.
- **Logische Operationen:** AND, OR, NOT, XOR.
- **Vergleiche:** Größer, kleiner, gleich.

### 2. Steuerwerk (CU - Control Unit)
Das Steuerwerk koordiniert alle Abläufe im Prozessor:
- Es liest Befehle aus dem Speicher (Fetch).
- Es dekodiert die Befehle (Decode) und entscheidet, welche Schaltungen aktiviert werden müssen.
- Es steuert den Datenfluss zwischen ALU, Registern und Hauptspeicher.

### 3. Registersatz (Registers)
Register sind extrem schnelle, kleine Speicherzellen direkt in der CPU. Sie dienen als Zwischenspeicher für laufende Berechnungen.
- **Datenregister / Akkumulator:** Speichert Operanden und Ergebnisse der ALU.
- **Befehlszähler (Program Counter - PC):** Enthält die Speicheradresse des *nächsten* auszuführenden Befehls.
- **Befehlsregister (Instruction Register - IR):** Speichert den aktuell in Ausführung befindlichen Befehl.
- **Statusregister (Flags):** Speichert Zustandswerte (z. B. Überlauf, Zero-Flag nach einer Subtraktion).

## Der Von-Neumann-Zyklus (Befehlszyklus)
Die CPU arbeitet Programme in einer endlosen Schleife ab:
1. **Fetch:** Befehl aus dem Speicher (an der Adresse des Program Counters) holen.
2. **Decode:** Den Befehl im Steuerwerk entschlüsseln.
3. **Fetch Operands:** Benötigte Daten (Operanden) aus dem Speicher oder Registern holen.
4. **Execute:** Befehl durch die ALU ausführen.
5. **Write Back:** Ergebnis in ein Register oder den Speicher zurückschreiben.

## Lernkarten #Rechnerarchitektur
Q: Welche Aufgaben hat die ALU (Arithmetic Logic Unit) in einem Prozessor?
A: Die Ausführung von arithmetischen Berechnungen (z.B. Addition) und logischen Verknüpfungen (z.B. AND, OR) sowie Vergleichen.

Q: Wozu dient der Program Counter (Befehlszähler) innerhalb der CPU?
A: Er speichert die Speicheradresse des **nächsten** auszuführenden Befehls, damit das Steuerwerk weiß, wo im Programm es nach dem aktuellen Befehl weitergeht.

Q: Benenne die klassischen Phasen des Befehlszyklus (Instruction Cycle).
A: Fetch (Befehl holen), Decode (Befehl dekodieren), Fetch Operands (Operanden holen), Execute (Ausführen), Write Back (Ergebnis speichern).
