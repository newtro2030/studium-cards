![[Pasted image 20260408145215.png]]

## Wasserfallmodell

Das erste beschriebene Vorgehensmodell der Softwareentwicklung. Bezugspunkt für fast alle anderen Vorgehensmodelle – eigentlich ein **Negativbeispiel**.

### Phasen (sequenziell)
1. [[Machbarkeitsstudie]] → Artefakt: Lastenheft, Projektkalkulation
2. [[Anforderungsanalyse]] → Artefakt: Pflichtenheft
3. [[Softwareentwurf]] → Artefakt: Architektur, Feinentwurf
4. [[Implementierung und Test]] → Artefakt: Programme, Testprotokolle
5. [[Auslieferung und Installation]] → Artefakt: Live-System, Handbücher
6. [[Wartung]]

### Merkmale
- Entwicklung in **sequenziellen Phasen**
- Phasen werden vollständig abgearbeitet, bevor fortgefahren wird
- Kundenbeteiligung nur am Anfang
- Phasen erzeugen **Artefakte**, die an nächste Phase übergeben werden
- Phasenübergänge mit **Meilensteinen** (formale Abnahme = *Reviews*)
- Erweiterung: Verifikation der Phasenprodukte vor Beginn der Folgephase

### Vorteile
- Klare Definition und Abgrenzung von Phasen, Rollen
- Lineare Struktur ermöglicht einfache Projektkontrolle und -planung
- Stabile Anforderungen erlauben genaue Kostenabschätzung
- Vielzahl von Dokumenten: leichte Mitarbeitereinarbeitung, Dokumentationspflichten erfüllt
- Fehler in frühen Phasen kostengünstiger zu beheben (Faktor 50–200)
- Geeignet für: Projekte mit stabilen Anforderungen oder sicherheitskritische Systeme

### Probleme / Nachteile
- Kosten-/Ressourcenschätzungen nur ungenau zu Projektbeginn möglich
- [[Wartung]] mit >60% Aufwand – aber nur eine von vielen Phasen
- Anwender können Feedback erst bei Produktfertigstellung geben
- Anforderungen am Projektanfang schwer festzulegen bei sich ändernden Anforderungen
- Phaseneinteilung strikt sequenziell – in Praxis meist nicht realistisch
- **Rücksprung nicht vorgesehen!** (Problem/Backlog, wenn Installation nicht klappt)
- Risikomanagement nur minimal (**Big Bang** am Ende der Entwicklung)
- Modell ist dokumentenlastig

### Alternativen
- [[V-Modell]] (Fokus: Qualitätssicherung)
- [[Inkrementelle Vorgehensmodelle]]
- [[Spiralmodell]]
- [[Rational Unified Process]]
