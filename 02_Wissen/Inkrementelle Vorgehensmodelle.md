## Inkrementelle Vorgehensmodelle

Weiterentwicklung des [[Wasserfallmodell]]s. Statt das Gesamtsystem in gesamter Breite zu entwickeln, wird es in **unabhängig entwickelbare Teilsysteme (Inkremente)** zerlegt.

### Grundidee
- [[Wasserfallmodell]]: sequenzielle Entwicklung des Gesamtsystems in aufeinanderfolgenden Phasen
- Inkrementell: Zergliederung in unabhängig entwickelbare Teilsysteme
- Vermeidung des monolithischen "Big Bang" am Ende der Entwicklung

### Struktur
1. **Anforderungsanalyse** (global, für alle Inkremente)
2. **Globaler Systementwurf** (Gesamtarchitektur)
3. **Pro Inkrement:** Detaillierter Entwurf → Implementierung → Test
4. **Auslieferung und Installation** (Gesamtsystem)

### Vorteile gegenüber Wasserfallmodell
- Flexibilität bei sich ändernden oder unklaren Anforderungen
- Testen und Feedback früher für Teilsysteme möglich
- "Lernen" aus frühen Inkrementen für weitere Entwicklung möglich
- Risikominimierung durch frühe Lieferung lauffähiger Teilsysteme

### Beispiele inkrementeller Modelle
- [[Rational Unified Process]] (RUP)
- [[Spiralmodell]]
- Agile Methoden (z.B. Scrum)

Siehe auch: [[Softwareprototypen]], [[Softwareentwicklung]]
