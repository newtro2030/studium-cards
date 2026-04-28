# Cache (Pufferspeicher)
#Rechnerarchitektur #Speicher

Der **Cache** ist ein kleiner, extrem schneller Zwischenspeicher (aus SRAM), der sich zwischen der CPU und dem Hauptspeicher befindet. Er dient dazu, den langsamen Zugriff auf den Hauptspeicher (DRAM) zu minimieren ("Verstecken der Zugriffslücke").

## Funktionsweise
Wenn die CPU Daten benötigt, sucht sie diese zuerst im Cache:
- **Cache Hit (Treffer):** Die Daten sind im Cache vorhanden. Die CPU kann verzögerungsfrei weiterarbeiten.
- **Cache Miss (Fehlschlag):** Die Daten sind nicht im Cache. Sie müssen aus dem langsameren Hauptspeicher geholt werden. Dabei wird nicht nur das angeforderte Byte, sondern ein ganzer Speicherblock (**Cache Line**) in den Cache geladen.

## Lokalitätsprinzipien
Der Cache funktioniert so gut, weil Computerprogramme auf Daten und Befehle nicht rein zufällig zugreifen, sondern sich nach dem Lokalitätsprinzip verhalten:
1. **Zeitliche Lokalität (Temporal Locality):** Wenn auf eine Speicheradresse zugegriffen wurde, ist die Wahrscheinlichkeit sehr hoch, dass auf *dieselbe* Adresse in naher Zukunft erneut zugegriffen wird (z. B. Schleifenvariablen, wiederholte Methodenaufrufe).
2. **Räumliche Lokalität (Spatial Locality):** Wenn auf eine Speicheradresse zugegriffen wurde, ist die Wahrscheinlichkeit sehr hoch, dass in naher Zukunft auf *benachbarte* Speicheradressen zugegriffen wird (z. B. Durchlaufen von Arrays, sequenzielles Abarbeiten von Programmcode).

## Cache-Level
Moderne CPUs nutzen eine mehrstufige Cache-Architektur (Multi-Level-Cache):
- **L1-Cache (Level 1):** Direkt im CPU-Kern. Winzig (oft 32-64 KB), aber rasend schnell. Oft aufgeteilt in Befehls-Cache (Instruction Cache) und Daten-Cache (Data Cache).
- **L2-Cache (Level 2):** Etwas langsamer, aber größer (z. B. 256 KB - 1 MB pro Kern).
- **L3-Cache (Level 3):** Wird oft von allen CPU-Kernen (Shared Cache) gemeinsam genutzt. Größer (mehrere MB), aber langsamer als L1 und L2.

## Lernkarten #Rechnerarchitektur
Q: Erkläre den Begriff "Cache Miss".
A: Ein Cache Miss tritt auf, wenn die CPU ein Datum im Cache sucht, es dort aber nicht findet. Das Datum muss dann zeitaufwändig aus der nächsttieferen Speicherebene (meist Hauptspeicher) nachgeladen werden.

Q: Auf welchen zwei physikalischen Beobachtungen basiert der Erfolg von Caches? (Lokalitätsprinzip)
A: Auf der **räumlichen Lokalität** (auf benachbarte Daten wird oft kurz hintereinander zugegriffen, z.B. Arrays) und der **zeitlichen Lokalität** (auf dieselben Daten wird oft mehrmals zugegriffen, z.B. Schleifenvariablen).

Q: Was ist eine "Cache Line"?
A: Ein zusammenhängender Block von Bytes, der bei einem Cache Miss aus dem RAM in den Cache geladen wird. Damit nutzt man die räumliche Lokalität aus.
