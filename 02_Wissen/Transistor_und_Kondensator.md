# Elektronische Grundbausteine: Transistor & Kondensator
#Rechnerarchitektur #Hardware #Elektrotechnik

Um zu verstehen, wie Computer auf unterster Ebene Daten speichern und verarbeiten, muss man die zwei wichtigsten elektronischen Bauteile kennen: den **Transistor** und den **Kondensator**.

## 1. Der Transistor (als Schalter)
In der modernen Rechnerarchitektur (insbesondere bei CPUs und RAM) werden Transistoren (meist MOSFETs) primär als **elektronische Schalter** verwendet. Sie besitzen keine mechanischen Teile und werden nur durch elektrische Spannung gesteuert.

### Aufbau und Funktion (vereinfacht)
Ein Feldeffekttransistor hat drei wesentliche Anschlüsse:
- **Source (Quelle):** Hier liegt der Strom an.
- **Drain (Abfluss):** Hier soll der Strom hin.
- **Gate (Gatter/Tor):** Der Steuereingang.

**Das Prinzip:** 
Zwischen Source und Drain befindet sich eine Barriere. Legt man am **Gate** eine Spannung an, entsteht ein elektrisches Feld, das diese Barriere öffnet. Der Strom kann von Source zu Drain fließen. 
- **Zustand 1 (Ein):** Spannung am Gate -> Strom fließt -> Logische "1".
- **Zustand 0 (Aus):** Keine Spannung am Gate -> Stromkreis unterbrochen -> Logische "0".

*In CPUs bilden Millionen solcher Transistoren logische Gatter (AND, OR, NOT), die wiederum das Rechenwerk (ALU) bilden.*

## 2. Der Kondensator (als Datenspeicher)
Ein Kondensator ist ein passives Bauteil, das elektrische Ladung (und damit Energie) in einem elektrischen Feld speichern kann. 

### Aufbau und Funktion
Er besteht im Wesentlichen aus zwei leitfähigen Platten (Elektroden), die durch eine isolierende Schicht (Dielektrikum) voneinander getrennt sind.
- Wird eine Spannung angelegt, sammeln sich Elektronen auf der einen Platte, während sie auf der anderen abgezogen werden. Der Kondensator lädt sich auf.
- **Zustand 1:** Kondensator ist geladen.
- **Zustand 0:** Kondensator ist entladen.

**Das Problem der Leckströme:**
Kein Isolator ist perfekt. Mit der Zeit (in Millisekunden) "versickert" die Ladung. Ein geladener Kondensator (1) verliert seine Spannung und wird zu einer 0. Das ist der Grund, warum DRAM-Speicher ständig "aufgefrischt" (refreshed) werden müssen.

## Zusammenspiel in einer DRAM-Speicherzelle (1-Bit)
Eine typische DRAM-Zelle (Hauptspeicher) besteht aus exakt **einem Kondensator** und **einem Transistor**:
1. Der **Kondensator** ist der eigentliche "Eimer", der die elektrische Ladung (das Bit) speichert.
2. Der **Transistor** fungiert als Tür (Access-Transistor). Er ist mit der Wortleitung (Steuerung) und der Bitleitung (Daten) verbunden.
3. **Schreiben/Lesen:** Soll das Bit gelesen oder geschrieben werden, gibt das Steuerwerk Spannung auf das Gate des Transistors. Der Schalter schließt sich und verbindet den Kondensator mit der Bitleitung, wodurch die Ladung ausgelesen oder neu hineingeschrieben werden kann.

## Lernkarten #Rechnerarchitektur
Q: Welche Funktion erfüllt der Transistor in einer modernen CPU oder einer DRAM-Zelle hauptsächlich?
A: Er fungiert als **elektronischer Schalter**, der ohne mechanische Bauteile allein durch das Anlegen einer Steuerspannung (am Gate) den Stromfluss öffnet (1) oder schließt (0).

Q: Wie speichert ein Kondensator Informationen und was ist sein größter Nachteil im Arbeitsspeicher (DRAM)?
A: Er speichert ein Bit in Form von elektrischer Ladung auf zwei isolierten Platten (Geladen = 1, Entladen = 0). Sein Nachteil ist, dass er diese Ladung durch Leckströme schnell verliert und das System ihn daher zyklisch neu auslesen und wieder aufladen muss (Refresh).

Q: Aus welchen zwei Bauteilen besteht eine typische DRAM-Speicherzelle und welche Rollen haben sie?
A: Aus **einem Kondensator** (speichert die eigentliche Ladung/das Bit) und **einem Transistor** (dient als Schalter/Tür, um den Kondensator zum Lesen oder Schreiben mit der Datenleitung zu verbinden).
