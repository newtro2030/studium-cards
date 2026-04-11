# Dijkstra-Algorithmus

### Zweck
Der Dijkstra-Algorithmus wird in **Link-State-Routing-Protokollen** (wie OSPF) verwendet, um den Pfad mit den **geringsten Kosten** (Shortest Path) von einem Quellknoten zu allen anderen Knoten in einem Netzwerk zu berechnen.

### Voraussetzungen
- Kennen der gesamten Netzwerktopologie (Link-State-Datenbank).
- Kosten an den Kanten (Links) müssen positiv sein.

### Schritt-für-Schritt Ablauf

1.  **Initialisierung**:
    - Setze die Kosten zum Startknoten auf **0**.
    - Setze die Kosten zu allen anderen Knoten auf **unendlich** ($\infty$).
    - Markiere alle Knoten als **unbesucht**.
2.  **Knoten wählen**:
    - Wähle den unbesuchten Knoten mit den **geringsten Kosten** als aktuellen Knoten.
3.  **Nachbarn aktualisieren**:
    - Für jeden unbesuchten Nachbarn des aktuellen Knotens: Berechne die Summe aus den Kosten des aktuellen Knotens + den Kosten der Kante zum Nachbarn.
    - Wenn dieser Wert **kleiner** ist als der bisher gespeicherte Wert des Nachbarn, aktualisiere die Kosten des Nachbarn.
4.  **Abschluss**:
    - Markiere den aktuellen Knoten als **besucht**. Ein besuchter Knoten wird nicht mehr verändert.
    - Wiederhole ab Schritt 2, bis alle Knoten besucht wurden.

> **Merksatz:** Dijkstra findet immer den billigsten Weg, indem er schrittweise den Wald der Möglichkeiten von "nah" nach "fern" erkundet.

→ Siehe auch: [[IPv4-Routing]] | [[OSI- und TCP-IP-Modell]]

## Lernkarten #Rechnernetze

Q: Was ist das Ziel des Dijkstra-Algorithmus im Kontext von Rechnernetzen?
A: Die Berechnung der Pfade mit den **geringsten Kosten** von einem Router zu allen anderen Routern im Netzwerk (Berechnung der Routingtabelle).

Q: In welcher Art von Routing-Protokollen wird Dijkstra eingesetzt?
A: In **Link-State-Protokollen** (z. B. OSPF).

Q: Nenne die 3 wesentlichen Schritte des Dijkstra-Algorithmus.
A: 1. Initialisierung (Start=0, Rest=$\infty$). 2. Den unbesuchten Knoten mit dem kleinsten Wert wählen. 3. Kosten der Nachbarn aktualisieren (Relaxierung).

Q: Warum müssen Kosten bei Dijkstra positiv sein?
A: Da der Algorithmus davon ausgeht, dass ein einmal besuchter Knoten bereits seinen optimalen (kleinsten) Wert hat. Bei negativen Kosten könnte ein späterer Pfad den Wert wieder senken, was die Logik bricht.
