# Dynamische Amortisationsrechnung

#konzept #investitionsrechnung #dynamisch

## Definition
Die dynamische Amortisationsrechnung ermittelt – wie die [[Statische Amortisationsrechnung|statische Variante]] – die Zeitspanne bis zum Kapitalrückfluss, berücksichtigt dabei jedoch den **Zeitwert des Geldes** durch Abzinsung der einzelnen Zahlungen auf den Zeitpunkt $t_0$.

## Einordnung
Gehört zu den **dynamischen Verfahren** (wie [[Kapitalwertmethode]], [[Interner Zinsfuß]], [[Annuitätenmethode]]). Dynamische Verfahren arbeiten mit konkreten Zahlungsreihen statt Durchschnittswerten.

## Vorgehensweise

1. Alle zukünftigen Zahlungen $Z_t$ werden mit dem Kalkulationszinssatz $i$ auf $t_0$ abgezinst:
$$BW_t = \frac{Z_t}{(1+i)^t}$$

2. Die abgezinsten Zahlungen werden kumuliert aufaddiert (inkl. der negativen Anfangsauszahlung).

3. Die **Amortisation** tritt ein, sobald die kumulierten Barwerte erstmals **≥ 0** werden.

4. Exakte Amortisationsdauer per linearer Interpolation:
$$t_{Amort} = t_{vorher} + \frac{|KW_{vorher}|}{BW_t}$$

## Entscheidungsregel
- **Einzelentscheidung:** Investition vorteilhaft, wenn Amortisation innerhalb der Nutzungsdauer
- **Auswahlentscheidung:** Wähle die Alternative mit der **kürzesten dynamischen Amortisationsdauer**

## Zusammenhänge
- Statische Variante ohne Abzinsung: [[Statische Amortisationsrechnung]]
- Verwandtes dynamisches Verfahren mit Fokus auf Wertzuwachs: [[Kapitalwertmethode]]
- Verwandtes Verfahren mit Fokus auf Verzinsung: [[Interner Zinsfuß]]
- Rechenbeispiel siehe [[KV IuF Aufgaben|Übungsblock 1, Aufgabe 4]]
