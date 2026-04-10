## Testpyramide

Die Testpyramide beschreibt die empfohlene Verteilung von Tests in einem Softwareprojekt – von vielen schnellen Unit-Tests an der Basis bis zu wenigen langsamen End-zu-Ende-Tests an der Spitze.

### Ebenen (von unten nach oben)
1. [[Unit-Tests]] (Komponententests) – sehr viele, sehr schnell
2. [[Integrationstests]] – mittel
3. [[Systemtest]] – wenige
4. [[Abnahmetest - End-zu-End-Test|Abnahmetest / End-zu-Ende-Tests]] – sehr wenige, langsam

### Grundprinzip
- Je höher in der Pyramide, desto teurer, langsamer, und weniger Tests
- Breite Basis: viele [[Unit-Tests]] sind kostengünstig und schnell
- Fehler früh (in unteren Ebenen) zu finden ist günstiger als spät

### Einordnung
- Im [[V-Modell]]: Die Testpyramide beschreibt die Testphasen auf der rechten Seite
- In [[Implementierung und Test]]: Alle Ebenen werden durchlaufen
