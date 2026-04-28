# Speicherhierarchie
#Rechnerarchitektur #Speicher

Die **Speicherhierarchie** (Speicherpyramide) ist ein zentrales Konzept der Rechnerarchitektur. Sie löst den Konflikt zwischen Speichergeschwindigkeit, Speicherkapazität und Kosten. 

## Die Ebenen der Hierarchie
Je näher ein Speicher an der CPU ist, desto schneller, teurer und kleiner ist er.

1. **Register:**
   - **Ort:** Direkt in der CPU.
   - **Geschwindigkeit:** Am schnellsten (Taktzyklus der CPU, < 1 ns).
   - **Kapazität:** Sehr gering (wenige Bytes, z.B. 64-Bit pro Register).
2. **Cache (L1, L2, L3):**
   - **Ort:** In oder sehr nah an der CPU.
   - **Technologie:** **SRAM** (Static RAM).
   - **Geschwindigkeit:** Sehr schnell (~1 bis 10 ns).
   - **Kapazität:** Gering (Kilobytes bis wenige Megabytes).
3. **Hauptspeicher (Arbeitsspeicher / RAM):**
   - **Ort:** Auf dem Mainboard.
   - **Technologie:** **DRAM** (Dynamic RAM).
   - **Geschwindigkeit:** Mittel (~50 bis 100 ns).
   - **Kapazität:** Groß (Gigabytes).
4. **Sekundärspeicher (Massenspeicher):**
   - **Ort:** Intern oder extern angeschlossen (SSD, HDD).
   - **Geschwindigkeit:** Langsam (Mikrosekunden bei SSDs bis Millisekunden bei HDDs).
   - **Kapazität:** Sehr groß (Terabytes).
5. **Tertiärspeicher (Archivspeicher):**
   - **Ort:** Oft offline (Magnetbänder, optische Datenträger).
   - **Geschwindigkeit:** Sehr langsam (Sekunden bis Minuten).
   - **Kapazität:** Riesig und kostengünstig.

## Die Zugriffslücke (Memory Wall)
Die sogenannte "Zugriffslücke" beschreibt den signifikanten Geschwindigkeitsunterschied zwischen dem extrem schnellen CPU-Cache und dem verhältnismäßig langsamen Hauptspeicher (DRAM) oder den Massenspeichern.

## Lernkarten #Rechnerarchitektur
Q: Warum gibt es eine Speicherhierarchie in Computern und nicht nur einen einzigen riesigen, schnellen Speicher?
A: Ein Speicher, der gleichzeitig extrem schnell, riesig und billig ist, ist physikalisch und ökonomisch unmöglich. Die Hierarchie kombiniert kleine, schnelle, teure Speicher (Cache) mit großen, langsamen, billigen Speichern (HDD/SSD), um die Illusion eines großen UND schnellen Speichers zu erzeugen.

Q: Ordne folgende Speicherarten nach Geschwindigkeit (schnellster zuerst): RAM, Register, SSD, L1-Cache.
A: Register > L1-Cache > RAM > SSD
