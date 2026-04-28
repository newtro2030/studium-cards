Erweiterung des [[Wasserfallmodell]]s durch explizite Zuordnung von **Qualitätssicherungsmaßnahmen** zu jeder Entwicklungsphase.

### Grundidee
- [[Wasserfallmodell]]: Integration und Test erst am Ende der Entwicklung (*Big-Bang-Integration*)
- V-Modell: Jeder Entwicklungsphase (links) entspricht eine **korrespondierende Testphase** (rechts)
- Fokus auf **Validierung** und **Verifikation** der Entwicklungsergebnisse

### Struktur des V

**Linke Seite – Entwicklung (absteigend, zunehmende Detaillierung):**
1. [[Systemanforderungsanalyse|Systemanforderungsanalyse]]
2. [[Systemarchitektur]]
3. [[System-Entwurf]]
4. [[Softwarearchitektur]]
5. Software-Entwurf (Boden des V)

**Rechte Seite – Tests (aufsteigend):**
5. [[Unit-Tests]] ↔ *Softwarearchitektur*
4. [[Integrationstests]] ↔ *System-Entwurf*
3. [[Systemtest]] (System-Integration) ↔ *Systemarchitektur*
2. [[Abnahme und Nutzung]] ↔ *Systemanforderungsanalyse*

**Ebenen:**
- Obere Ebene: **Validierung** – Wurde das richtige System gebaut?
- Untere Ebenen: **Verifikation** – Wurde das System richtig gebaut?

### Vorteil
- Expliziter **Fokus auf Qualitätssicherung** – Testphasen werden von Beginn an mitgeplant
- Fehler werden früher erkannt

### Nachteil
- Andere Nachteile des [[Wasserfallmodell]]s bleiben erhalten (kein früher Kundenfeedback, starre Phasen)

### Weiterentwicklungen
- **V-Modell XT**: Standard-Vorgehensmodell der öffentlichen Hand in Deutschland
- V-Modell als Vorgehensmodell im Kontext Softwaretest (Testpyramide)
