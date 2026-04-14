## Strukturierte Analyse und Entwurf

Methode der Softwareentwicklung der **1980/90er Jahre**. Problem wird getrennt in Datenaspekte und Verhaltensaspekte modelliert.

### Modellierung von Verhaltensaspekten
- **Datenflussdiagramme**: Darstellung von Datenflüssen zwischen Prozessen, externen Entitäten und Datenspeichern
  - Elemente: Datenfluss (Pfeil), Prozess (Kreis), extern (Rechteck), Datenspeicher (Doppellinie)
- **Funktionsbäume** (*Structure Charts*): hierarchische Zerlegung in Module

### Modellierung von Datenaspekten/-strukturen
- **Datenwörterbücher** (*Data Dictionaries*)
- **Entity-Relationship-Diagramme**: Entitäten, Relationen, Attribute mit Kardinalitäten

### Modellierung von Algorithmen
- Flussdiagramme, Struktogramme
- Entscheidungstabellen
- Pseudocode

### Modellierung zustandsbehafteter Systeme
- **Zustandsübergangsdiagramme**: Zustände und Übergänge mit Ereignissen
- *Petrinetze*

### Übergang Analyse → Entwurf
- Produkt der strukturierten Analyse: Datenflussdiagramm
- Ableitung der Softwarearchitektur in der Entwurfsphase
- Hierarchische Strukturierung in Module

### Nachteile der strukturierten Methode
- Sehr starke **Trennung zwischen Daten- und Verhaltensaspekten**
  - Konsistenz zwischen Modellen muss explizit sichergestellt werden
  - Modellierung oft entweder nur für Daten oder für Verhalten
- Unterschiedliche Methoden/Werkzeuge in Analyse und Entwurf
  - Trennung zwischen Analyse und Entwurf auch erwünscht, aber Konsistenz schwierig

### Wünschenswert
- Modellierungsmethoden und -werkzeuge **phasenübergreifend**
- Integration der Daten- und Verhaltensmodellierung
→ Lösung: [[Objektorientierte Modellierung]]

→ Siehe auch: [[Softwareentwicklung]] | [[Softwareentwurf]]
