## Lernkarten #MPP_kurz

Q: Was ist die Stacey-Matrix?
A: - Modell zur Projekteinordnung nach 2 Achsen: Klarheit der Anforderungen (WAS) × technische Unsicherheit (WIE)
- 4 Zonen → passende Methode: Einfach → Wasserfall, Kompliziert → Kanban, Komplex → Scrum, Chaotisch → Design Thinking
- Hilft bei der Wahl zwischen klassischem und agilem Vorgehen

Q: Wie schreibe ich eine einfache Klasse? (Beispiel Java)
A: Eine Klasse bündelt Attribute (Daten) und Methoden (Verhalten):
class Auto {
  private String marke;
  private int ps;
  public void fahren() { System.out.println("faehrt"); }
}
- Objekt erzeugen: Auto a = new Auto();
- Attribute meist private (Kapselung), Zugriff über Methoden

Q: Werkvertrag vs. Dienstvertrag?
A: - Werkvertrag (§ 631 BGB): ein konkreter Erfolg/Werk geschuldet, Abnahme nötig, Gewährleistung bei Mängeln (z.B. fertige Software)
- Dienstvertrag (§ 611 BGB): nur die Tätigkeit geschuldet, kein bestimmter Erfolg (z.B. Beratung, Arbeitsvertrag)
- Merksatz: Werk = Ergebnis, Dienst = Bemühen

Q: Was umfasst das EGovG (ThürEGovG, OZG)?
A: - EGovG = Gesetz zur Förderung der elektronischen Verwaltung (Bund 2013, Thüringen: ThürEGovG)
- Inhalte: elektronischer Zugang zur Behörde, E-Akte, ersetzendes Scannen, elektronische Bezahlung, OpenData, Abbau von Schriftformerfordernissen
- OZG (Onlinezugangsgesetz) ergänzt: Verwaltungsleistungen online über Portalverbund anbieten

Q: Unterschied SQL- und NoSQL-Datenbanken?
A: - SQL (relational): feste Tabellen mit Schema, Beziehungen, ACID-konform, SQL-Abfragesprache (MySQL, PostgreSQL)
- NoSQL (nicht-relational): flexibles/schemafreies Modell, horizontal skalierbar, große Datenmengen (MongoDB, Redis)
- SQL für strukturierte Daten mit klaren Beziehungen, NoSQL für große, unstrukturierte/wechselnde Daten

Q: Welche Gesellschaftsformen gibt es?
A: - Einzelunternehmen: eine Person, volle persönliche Haftung
- Personengesellschaften (GbR, OHG, KG): mind. 2 Personen, persönliche Haftung der Gesellschafter
- Kapitalgesellschaften (GmbH, UG, AG): juristische Person, Haftung auf Einlage beschränkt
- GmbH: 25.000 € Stammkapital; AG: 50.000 € Grundkapital; Mischform: GmbH & Co. KG

Q: Wie erkläre/zeichne ich eine Bilanz?
A: - Gegenüberstellung von Vermögen und Kapital zu einem Stichtag, beide Seiten immer gleich hoch
- Skizze als T-Konto: LINKS Aktiva (Mittelverwendung) = Anlagevermögen + Umlaufvermögen
- RECHTS Passiva (Mittelherkunft) = Eigenkapital + Fremdkapital
- Grundgleichung: Summe Aktiva = Summe Passiva

Q: Unterschied Inner Join und Left Join?
A: - Inner Join: nur Zeilen, die in BEIDEN Tabellen einen passenden Treffer haben (Schnittmenge)
- Left Join: ALLE Zeilen der linken Tabelle + passende der rechten; fehlt rechts ein Treffer → NULL
- Merksatz: Inner = nur Übereinstimmungen, Left = links komplett behalten

Q: Was ist die BCG-Matrix?
A: - Portfolio-Analyse nach Marktanteil × Marktwachstum, 4 Felder:
- Stars: hoher Anteil + hohes Wachstum → investieren
- Cash Cows: hoher Anteil + niedriges Wachstum → Gewinne abschöpfen
- Question Marks: niedriger Anteil + hohes Wachstum → selektiv fördern
- Poor Dogs: niedriger Anteil + niedriges Wachstum → desinvestieren

Q: Was ist eine Variable? (Speicher + Initialisierung)
A: - Benannter Speicherplatz für einen Wert mit drei Merkmalen:
- Größe: durch den Datentyp bestimmt (z.B. int = 4 Byte)
- Adresse: physischer Ort im Arbeitsspeicher
- Symbolischer Name: Bezeichner, über den der Programmierer zugreift
- Initialisierung = erste Wertzuweisung bei der Deklaration, z.B. int x = 5;
- Skizze: Kästchen mit Name darüber, Adresse darunter, Wert (5) im Kästchen

Q: Was ist das OSI-Modell?
A: - Referenzmodell mit 7 Schichten für Netzwerkkommunikation:
- 1 Bitübertragung, 2 Sicherung, 3 Vermittlung (IP), 4 Transport (TCP/UDP), 5 Sitzung, 6 Darstellung, 7 Anwendung
- Jede Schicht hat feste Aufgaben und nutzt die Dienste der darunterliegenden
- Merksatz: "Alle Deutschen Studenten Trinken Verschiedene Sorten Bier" (7→1)

Q: Welche Netzwerktopologien gibt es? (mit Beispielen)
A: - Stern: zentraler Knoten (Switch), Beispiel modernes Heim-/Büronetz
- Bus: gemeinsame Leitung, Beispiel altes Ethernet (10Base2)
- Ring: geschlossener Kreis, Beispiel Token Ring, FDDI
- Masche: viele Querverbindungen, Beispiel Internet, WLAN-Mesh
- Baum: hierarchische Verkettung von Sternen

Q: Was ist bei einer Projektarbeit (PA) wichtig?
A: - Eigenständige wissenschaftliche Bearbeitung einer praxisnahen Fragestellung
- Aufbau: Einleitung (Problem/Ziel) → Hauptteil (Methodik, Analyse, Umsetzung) → Schluss (Fazit, Ausblick)
- Formale Anforderungen: Gliederung, Zitierweise/Quellen, Literaturverzeichnis, Eigenständigkeitserklärung
- Vorgehen: Themenfindung, Zeitplan, Recherche, Schreiben, Korrektur

Q: Was ist ein Zeiger und was bedeutet Datenadressierung?
A: - Zeiger (Pointer): Variable, die nicht einen Wert, sondern eine Speicheradresse enthält (zeigt auf andere Daten)
- Dereferenzierung: über den Zeiger auf den Wert an der Adresse zugreifen
- Adressierungsarten: unmittelbar (Wert im Befehl), direkt (Adresse im Befehl), indirekt (Adresse zeigt auf Adresse), indiziert (Basisadresse + Index)

Q: Wie zähle ich Objekte einer Klasse mit?
A: - Statisches Klassenattribut verwenden (static), das zur Klasse gehört, nicht zum einzelnen Objekt
- Im Konstruktor bei jeder Objekterzeugung hochzählen: count++;
- Beispiel: private static int count = 0; im Konstruktor count++;
- Abruf über Klassenname, da klassengebunden (z.B. Auto.count)

Q: Was ist OpenData und wie soll es laut EGovG genutzt werden?
A: - Offene Daten: von Behörden frei zugängliche, maschinenlesbare Rohdaten ohne Nutzungsbeschränkung
- EGovG (§ 12a Bund): Behörden sollen Daten "open by default" bereitstellen – kostenfrei, strukturiert, weiterverwendbar
- Zweck: Transparenz, Bürgerbeteiligung, wirtschaftliche Wertschöpfung, Innovation

Q: Was ist ein Linker?
A: - Programm, das die vom Compiler erzeugten Objektdateien (.o) und Bibliotheken zu einem ausführbaren Programm zusammenbindet
- Löst Referenzen zwischen Modulen auf und vergibt endgültige Adressen
- Reihenfolge: Compiler (übersetzt) → Linker (bindet) → ausführbares Programm

Q: Was ist eGovernment (eGov)?
A: - Abwicklung von Verwaltungs- und Regierungsprozessen über digitale Medien (Internet)
- Beziehungen: G2C (Bürger), G2B (Unternehmen), G2G (Behörden untereinander)
- Ziel: schnellere, ortsunabhängige und effizientere Verwaltungsleistungen

Q: Was ist Digitalisierung?
A: - Im engeren Sinn: Umwandlung analoger Informationen in digitale (z.B. Akte einscannen)
- Im weiteren Sinn: Transformation von Prozessen, Strukturen und Geschäftsmodellen durch digitale Technologien
- In der Verwaltung: Grundlage für eGovernment, E-Akte, Online-Dienste

Q: Was ist der IT-Planungsrat?
A: - Gemeinsames Gremium von Bund und Ländern (Grundlage Art. 91c GG)
- Aufgaben: Steuerung der IT-Zusammenarbeit, Beschluss verbindlicher IT-Standards, Koordination des OZG
- Ziel: einheitliche, interoperable Verwaltungs-IT in Deutschland

Q: Was ist das BSI?
A: - Bundesamt für Sicherheit in der Informationstechnik – nationale Cyber-Sicherheitsbehörde
- Aufgaben: IT-Sicherheitsstandards (IT-Grundschutz), Beratung von Behörden/Unternehmen, Abwehr von Cyberangriffen
- Zentrale Stelle für Informationssicherheit in Deutschland

Q: Warum darf der Bund ein E-Gov-Gesetz (OZG) für alle Länder erlassen? (Art. 91c GG)
A: - Grundsätzlich haben die Länder die Verwaltungshoheit – der Bund bräuchte eine Kompetenzgrundlage
- Art. 91c GG wurde geschaffen, damit Bund und Länder beim IT-Einsatz zusammenwirken
- Art. 91c Abs. 5 GG erlaubt dem Bund, den übergreifenden Zugang zu Verwaltungsleistungen (Portalverbund) per Bundesgesetz mit Zustimmung des Bundesrates zu regeln → Grundlage des OZG

Q: Welche Vorgehensmodelle der Softwareentwicklung gibt es?
A: - Klassisch/schwergewichtig: Wasserfall (linear), V-Modell (mit Testphasen), Spiralmodell (mit Risikoanalyse)
- Agil/leichtgewichtig: Scrum, Kanban – iterativ und flexibel
- Inkrementell/iterativ: schrittweise Lieferung und Verfeinerung
- Wahl je nach Anforderungsklarheit und Risiko (vgl. Stacey-Matrix)

Q: Was ist die Von-Neumann-Architektur?
A: - Rechnerkonzept mit EINEM gemeinsamen Speicher für Daten UND Befehle
- Komponenten: CPU (Steuerwerk + Rechenwerk/ALU), Speicher, Ein-/Ausgabe, Bussystem
- Befehle werden sequentiell abgearbeitet
- Nachteil: Von-Neumann-Flaschenhals (Daten und Befehle teilen sich einen Bus)

Q: Erkläre Vererbung und Kapselung (mit Beispiel).
A: - Vererbung: Unterklasse übernimmt Attribute/Methoden der Oberklasse ("ist-ein"), z.B. Klasse PKW erbt von Fahrzeug; ermöglicht Wiederverwendung
- Kapselung: interne Daten verbergen, Zugriff nur über definierte Methoden (Getter/Setter), Attribute private
- Beispiel Kapselung: kontostand private, Änderung nur über einzahlen()/auszahlen()

Q: Unterschied RISC und CISC?
A: - RISC (Reduced Instruction Set): wenige, einfache Befehle, feste Länge, viele Register, schnelle Abarbeitung
- CISC (Complex Instruction Set): viele, komplexe Befehle, variable Länge, weniger Register
- RISC: einfacher Aufbau, hoher Takt (ARM); CISC: mächtige Einzelbefehle (x86)

Q: Unterschied Compiler und Interpreter? (Wo steht Java?)
A: - Compiler: übersetzt das GESAMTE Programm vorab in Maschinencode → schnelle Ausführung
- Interpreter: führt den Quellcode Zeile für Zeile zur Laufzeit aus → flexibel, aber langsamer
- Java ist hybrid: Compiler erzeugt plattformunabhängigen Bytecode, die JVM interpretiert ihn bzw. kompiliert ihn per JIT zur Laufzeit

Q: Unterschied Tarifvertrag und Arbeitsvertrag?
A: - Tarifvertrag: kollektiv zwischen Gewerkschaft und Arbeitgeber(verband), regelt Mindestbedingungen (Lohn, Arbeitszeit, Urlaub)
- Arbeitsvertrag: individuell zwischen einzelnem Arbeitnehmer und Arbeitgeber
- Günstigkeitsprinzip: der für den AN günstigere (meist Arbeitsvertrag) gilt, Tarif als Untergrenze

Q: Serieller vs. paralleler Bus?
A: - Seriell: Bits nacheinander über eine Leitung, weniger Störungen, sehr hohe Taktraten möglich (USB, SATA)
- Parallel: mehrere Bits gleichzeitig über mehrere Leitungen (altes PCI, IDE)
- Parallel bei hohem Takt problematisch (Laufzeitunterschiede/Skew) → heute meist seriell

Q: Was ist das Schriftformerfordernis?
A: - Gesetzlich vorgeschriebene Form mit eigenhändiger Unterschrift (§ 126 BGB)
- Ersetzbar durch elektronische Form mit qualifizierter elektronischer Signatur (§ 126a BGB)
- Beispiele Arbeitsrecht: Kündigung zwingend schriftlich (§ 623 BGB, keine E-Mail!), Befristung (§ 14 IV TzBfG)
- EGovG zielt auf den Abbau unnötiger Schriftformerfordernisse

Q: Welche Projektformen (Projektorganisation) gibt es?
A: - Reine Projektorganisation: eigenständige Einheit, Projektleiter hat volle Weisungsbefugnis
- Einfluss-/Stabsprojektorganisation: Projektleiter nur beratend, keine Weisungsbefugnis
- Matrix-Projektorganisation: geteilte Befugnis zwischen Projekt- und Abteilungsleitung
- Wahl je nach Projektgröße, Dauer und Bedeutung

Q: Was ist der Produktlebenszyklus und der Break-Even-Punkt?
A: - Phasen: Einführung → Wachstum → Reife → Sättigung → Rückgang/Degeneration
- Einführung: hohe Kosten, Verluste; Wachstum: steigende Umsätze
- Break-Even-Punkt: Punkt, an dem die Erlöse die Gesamtkosten decken (weder Gewinn noch Verlust)
- Liegt meist am Übergang Einführung → Wachstum; danach beginnt die Gewinnzone

Q: Was ist Pipelining?
A: - Technik in der CPU, bei der Befehlsphasen überlappend parallel ablaufen
- Phasen z.B.: Fetch, Decode, Execute, Write Back – während ein Befehl ausgeführt wird, wird der nächste schon geladen
- Erhöht den Durchsatz (mehr Befehle pro Zeit), nicht die Geschwindigkeit eines Einzelbefehls

Q: Was ist der PDCA-Zyklus? (anzeichnen + erläutern)
A: - Deming-Kreis für kontinuierliche Verbesserung (KVP), 4 Phasen im Kreis:
- Plan: Ziele setzen, Maßnahmen planen
- Do: Maßnahmen umsetzen (im Kleinen/Test)
- Check: Ergebnisse prüfen, mit Ziel vergleichen
- Act: bei Erfolg standardisieren, sonst anpassen
- Skizze: Kreis in 4 Segmente (P→D→C→A), der als Rad einen Hang aufwärts rollt (stetige Verbesserung)

Q: Was ist das OZG?
A: - Onlinezugangsgesetz (2017): verpflichtet Bund, Länder und Kommunen, Verwaltungsleistungen digital anzubieten
- Zugang über einen Portalverbund (vernetzte Verwaltungsportale)
- Kompetenzgrundlage: Art. 91c Abs. 5 GG
- Ziel: Bürger und Unternehmen erledigen Behördengänge online

Q: Was regelt das KSchG und welche Besonderheiten gibt es?
A: - Kündigungsschutzgesetz: schützt Arbeitnehmer vor sozial ungerechtfertigter Kündigung
- Gilt erst ab Betrieb > 10 Beschäftigte und nach 6 Monaten Wartezeit
- Kündigung nur wenn sozial gerechtfertigt: personen-, verhaltens- oder betriebsbedingt
- Besonderheiten: Sozialauswahl (bei betriebsbedingt), Sonderkündigungsschutz für Schwangere, Schwerbehinderte, Betriebsräte, Eltern in Elternzeit

Q: Was sind Konstruktor und Destruktor?
A: - Konstruktor: spezielle Methode, die ein Objekt bei der Erzeugung initialisiert (gleicher Name wie Klasse, kein Rückgabetyp)
- Destruktor: gibt beim Zerstören des Objekts Ressourcen frei (C++: ~Klassenname)
- Java: kein echter Destruktor – die Speicherfreigabe übernimmt der Garbage Collector

Q: Wie stellt man eine Klasse im UML-Diagramm dar?
A: - Rechteck mit drei Abschnitten (von oben nach unten):
- 1. Klassenname
- 2. Attribute (mit Datentyp)
- 3. Methoden (mit Parametern/Rückgabe)
- Sichtbarkeiten davor: + public, - private, # protected

Q: Was bedeutet Datenkapselung?
A: - Verbergen der internen Daten eines Objekts vor direktem Zugriff von außen
- Attribute werden private, der Zugriff erfolgt nur über öffentliche Methoden (Getter/Setter)
- Vorteil: Schutz vor unkontrollierten/ungültigen Änderungen, klare Schnittstelle, leichtere Wartung

Q: Was ist Cashflow?
A: - Saldo aus Einzahlungen und Auszahlungen einer Periode → Maß für die Innenfinanzierungskraft
- Zeigt, wie viel Geld ein Unternehmen tatsächlich erwirtschaftet (zahlungswirksam)
- Vereinfacht (indirekt): Gewinn + Abschreibungen + Rückstellungszuführungen
- Arten: operativer, investiver und Finanzierungs-Cashflow

Q: Was versteht man unter Büromanagement?
A: - Planung, Organisation und Steuerung aller Büroabläufe in einer Verwaltung/einem Unternehmen
- Aufgaben: Schriftgut-/Dokumentenverwaltung, Termin- und Vorgangsbearbeitung, Kommunikation, Beschaffung
- Unterstützung durch Bürokommunikationssysteme/DMS
- Ziel: effiziente, strukturierte und nachvollziehbare Verwaltungsabläufe

Q: Arbeitsverhältnis – Unterschied Beamte und Tarifbeschäftigte?
A: - Beamte: öffentlich-rechtliches Dienstverhältnis durch Ernennung, Treuepflicht, kein Streikrecht, Besoldung (BBesG), Versorgung (Pension) + Beihilfe
- Tarifbeschäftigte: privatrechtlicher Arbeitsvertrag, Vergütung nach TVöD/TV-L, Streikrecht, gesetzliche Sozialversicherung (Rente)
- Beamte für hoheitliche Aufgaben, Tarifbeschäftigte für übrige Tätigkeiten
