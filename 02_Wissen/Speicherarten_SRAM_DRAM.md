# Speicherarten: SRAM vs. DRAM
#Rechnerarchitektur #Speicher #Hardware

Der flüchtige Speicher (RAM - Random Access Memory) wird hardwaretechnisch hauptsächlich in zwei Kategorien unterteilt: **SRAM** und **DRAM**.

## SRAM (Static RAM)
SRAM speichert Daten mithilfe von **Flip-Flops** (bistabile Kippstufen, typischerweise aus 4 bis 6 Transistoren pro Bit).
- **Vorteile:**
  - Extrem schnell.
  - Muss nicht regelmäßig aufgefrischt ("refreshed") werden, solange Strom anliegt (daher "statisch").
- **Nachteile:**
  - Braucht viel Platz auf dem Chip (viele Transistoren pro Bit).
  - Sehr teuer in der Herstellung.
  - Höherer Stromverbrauch pro Bit.
- **Einsatzgebiet:** CPU-Caches (L1, L2, L3) und Register.

## DRAM (Dynamic RAM)
DRAM speichert Daten in Form von elektrischer Ladung in kleinen **Kondensatoren** (Kombination aus 1 Transistor + 1 Kondensator pro Bit).
- **Vorteile:**
  - Sehr hohe Speicherdichte (wenig Platz pro Bit).
  - Deutlich günstiger als SRAM.
- **Nachteile:**
  - Kondensatoren verlieren im Bruchteil einer Sekunde ihre Ladung. Daher müssen die Daten ständig neu gelesen und geschrieben werden (**Refresh-Zyklen**, daher "dynamisch").
  - Deutlich langsamer als SRAM.
- **Einsatzgebiet:** Hauptspeicher / Arbeitsspeicher des Computers.

## Gegenüberstellung

| Eigenschaft | SRAM (Static RAM) | DRAM (Dynamic RAM) |
| :--- | :--- | :--- |
| **Aufbau pro Bit** | Flip-Flop (4-6 Transistoren) | 1 Kondensator + 1 Transistor |
| **Geschwindigkeit** | Sehr hoch | Mittel |
| **Packungsdichte** | Gering | Sehr hoch |
| **Kosten** | Hoch | Gering |
| **Refresh nötig?** | Nein | Ja (periodisch) |
| **Typische Verwendung**| Cache (L1/L2/L3) | Hauptspeicher (RAM) |

## Lernkarten #Rechnerarchitektur
Q: Warum wird der Hauptspeicher aus DRAM und nicht aus dem viel schnelleren SRAM gebaut?
A: SRAM ist aufgrund der 4-6 Transistoren pro Bit viel zu teuer und benötigt zu viel Platz für große Kapazitäten. DRAM bietet eine viel höhere Dichte bei geringeren Kosten.

Q: Was bedeutet das "D" in DRAM und worauf bezieht es sich technisch?
A: "Dynamic". Es bezieht sich darauf, dass der Speicher seinen Zustand dynamisch aufrechterhalten muss. Die Speicherkondensatoren entladen sich kontinuierlich und müssen periodisch aufgefrischt (refreshed) werden.
