### Was ist ein Objekt?

 4 wichtige Prinzipien
 - 1. Vererbung -> Methoden werden weitergegeben an die Unterklassen
 - 2. Datenkapselung (Information Hiding)
	 - Grund: Kompatibilität (Wartbarkeit), Integrität, Vertraulichkeit
	 - Modifier: public, private, protected, default, package
- 3. Polymorphie -> Überschreiben
	- an verschiedene Objekte die selbe Nachricht schicken
	- Parametrische Polymorphie
- 4. Abstraktion
	- Bsp.: Handy, Laptop, Tablet sind Computer -> ein Computer hat bestimmte Attribute


![[Recording 20260423150954.m4a]]


 - Identität -> Objekte können nachrichten schicken (miteinander kommunizieren)
 - Attribut = Zustand
 - Methode = Verhalten
 - Nachrichtenaustausch
 - Objekte sind Instanz einer Klasse -> können also eine Schablone haben

- Objekte sind persistent über die Zeit (Programm beenden beim nächsten mal ist es wieder da)
- Objekte sind persistent über den Raum (Objekt kann von einem Rechner zum anderen übertragen werden können)

- Was ist eine Nachricht in JAVA?
	- Methodenaufruf = Nachricht

Wichtigste Grund ist die
- Wartbarkeit
- Wiederverwendbarkeit
- 
 
- a.mU) -> a Empfänger mU Nachricht Parameter

Objektidentität oder Objektgleichheit?

![[Recording 20260423152745.m4a]]

Öffentlicher Bereich vs. privater Bereich:
Abstrakte kann keine Objekte erzeugen

dynamisches Binden:
- Objekttyp erst zur Laufzeit


![[Recording 20260423160200.m4a]]


![[Recording 20260423160906.m4a]]


> "An object is a thing real or abstract about which we store data and those methods which manipulate the data." *(Robert Martin)*

> "An object has state, behavior, and identity." *(Grady Booch)*

Ein Objekt besitzt:
- **Unveränderliche Identität** (Objektbezeichner/Id, unabhängig vom Zustand)
- **Veränderlichen Zustand** (durch Zustandsvariablen/Attribute)
- **Dynamisches Verhalten** (durch Methoden/Operationen)

Wichtig: **Objektidentität ≠ Objektgleichheit** (Referenzsemantik)

### Zustand eines Objekts
- Wird durch **Zustandsvariablen** (Attribute) festgelegt
- Zustandsvariablen können primitiv oder Objektreferenzen sein
- Objektzustand kann sich während der Lebenszeit ändern

### Klassen
- Gleichartige Objekte werden in einer **Klasse** zusammengefasst
- Objekt ist **Instanz genau einer Klasse**
- Klassen sind **Schablonen** und legen fest:
  - Zustandsvariablen mit zugehörigen Wertebereichen
  - Unterstützte Operationen in Form von Methoden
  - Trennung in **Schnittstelle** (interface) und **Implementierung**
- Klassen setzen das Prinzip der **Datenkapselung** um
- **Abstrakte Klassen**: keine Instanzen, unvollständige Implementierung

### Vererbung (Spezialisierung)
- Ableitung von Klassen auf Basis bestehender Klassen
- Unterklassen erben von ihren Oberklassen (**is-a**-Beziehung):
  - Schnittstellendefinition
  - Methodenimplementierungen
  - Zustandsvariablen
- Unterklassen können:
  - Vererbtes Verhalten redefinieren (**Überschreiben**)
  - Zusätzliches Verhalten definieren
- Vererbung ist eine **transitive Beziehung** (Vererbungshierarchien)

#### Mehrfachvererbung
- In **Java**: Klasse kann mehrere Schnittstellen implementieren, aber nur eine Oberklasse erweitern
  - Ab Java 8: Mehrfachvererbung für Methodenimplementierungen möglich (default methods)
- In anderen Sprachen: Erweiterung mehrerer Oberklassen zulässig
- Problem: **Vererbungskonflikte** (verschiedene Methoden mit gleichem Namen)

### Polymorphie (Vielgestaltigkeit)
Erlaubt den Aufruf verschiedener Implementierungen über die gleiche Funktion.

Zwei Formen:
- **Überladen**: Auswahl anhand der Argumenttypen zur **Übersetzungszeit**
  ```java
  move(dx: Integer, dy: Integer) { x += dx; y += dy; }
  move(dx: Float, dy: Float) { x += round(dx); y += round(dy); }
  ```
- **Überschreiben**: Auswahl aus Methoden mit gleichen Namen und Argumenttypen zur **Laufzeit** (dynamisches Binden, virtuelle Methoden)
  ```java
  class Rectangle { void draw() { ... } }
  class ColoredRectangle extends Rectangle { void draw() { ... } }
  // r.draw() ruft je nach tatsächlichem Typ die richtige Methode auf
  ```

### Typen und Schnittstellen
- **Typ** eines Objekts legt fest, welche Operationen anwendbar sind
- Typen sind **Schnittstellendefinitionen** (*Interfaces*)
- Klassen implementieren im Allgemeinen **mehrere Schnittstellen**
- Statisch typisierte Sprachen garantieren, dass zur Laufzeit nie Methoden aufgerufen werden, die nicht implementiert sind

### Nachrichtenaustausch (Message Passing)
- Objekte kooperieren/kommunizieren über **Nachrichten**
- Nachrichtenaufbau: `Empfänger + Methodenname + Argumente`

Arten von Nachrichten:
- **Methodenaufruf**: Kommunikation zwischen sendendem und festgelegtem empfangendem Objekt
- **Signal**: Kommunikation an alle Objekte, die das Signal empfangen (Kanal)

Arten der Kommunikation:
- **Synchron**: Sender wartet auf Verarbeitung (Rückgabewert)
- **Asynchron**: Sender wartet nicht; Rückgabewert ggf. als separate Nachricht

### Vorteile der Objektorientierung
- **Wiederverwendung** durch Spezialisierung/Generalisierung und Design Patterns
- **Polymorphismus** durch dynamisches Binden und Überladen
- **Prototyping** durch schnelle Entwicklungszyklen und Wiederverwendung
- **Verteilte Systeme** durch Datenkapselung und Nachrichtenaustausch
- Einheitliche Modellierungsmethode/-werkzeuge

### Abstraktionsebenen
```
Realität (konkrete Objekte der realen Welt)
    ↑ Abstraktion
Modell: Objekte → Analysemodell → Entwurfsmodell → Programm (Quelltext)
    ↓ konkrete Objekte (z.B. in Java Virtual Machine)
```

→ Siehe auch: [[Objektorientierte Modellierung]] | [[OOP Java]] | [[Strukturierte Analyse und Entwurf]]
