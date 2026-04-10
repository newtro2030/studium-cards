# Kapitalwertmethode

#konzept #investitionsrechnung #dynamisch

## Definition
Die Kapitalwertmethode (auch: Net Present Value, NPV) ist das zentrale **dynamische** Investitionsrechenverfahren. Sie ermittelt den Barwert aller zukünftigen Ein- und Auszahlungen einer Investition, abgezinst auf den Zeitpunkt $t_0$.

## Einordnung
Gehört zu den **dynamischen Verfahren** (wie [[Interner Zinsfuß]], [[Dynamische Amortisationsrechnung]], [[Annuitätenmethode]]). Der Kapitalwert ist das theoretisch fundierteste Entscheidungskriterium der Investitionsrechnung.

## Formel

$$KW = \sum_{t=0}^{n} \frac{Z_t}{(1+i)^t} = -A_0 + \sum_{t=1}^{n} \frac{Z_t}{(1+i)^t}$$

Wobei:
- $A_0$ = Anfangsauszahlung (Investitionskosten)
- $Z_t$ = Nettozahlung (Einzahlung − Auszahlung) in Periode $t$
- $i$ = Kalkulationszinssatz
- $n$ = Nutzungsdauer / Planungshorizont

## Entscheidungsregel
- **Einzelentscheidung:** Investition vorteilhaft, wenn **$KW > 0$** (die Investition erwirtschaftet mehr als die geforderte Mindestverzinsung)
- **Auswahlentscheidung:** Wähle die Alternative mit dem **höchsten positiven Kapitalwert**

## Interpretation des Kapitalwerts
- $KW > 0$: Die Investition schafft über die Mindestverzinsung hinaus einen Mehrwert
- $KW = 0$: Die Investition erwirtschaftet genau die Mindestverzinsung (→ der Zinssatz ist der [[Interner Zinsfuß|interne Zinsfuß]])
- $KW < 0$: Die Investition erreicht die Mindestverzinsung nicht

## Vor- und Nachteile
| ✅ Vorteile | ❌ Nachteile |
|---|---|
| Theoretisch fundiert (Zeitwert des Geldes) | Abhängig vom gewählten Kalkulationszins |
| Berücksichtigt alle Zahlungen | Zukünftige Zahlungen müssen geschätzt werden |
| Eindeutiges Ergebnis (kein Mehrdeutigkeitsproblem) | Schwer verständlich für Nicht-Fachleute |

## Zusammenhänge
- Der [[Interner Zinsfuß|interne Zinsfuß]] ist der Zinssatz, bei dem der Kapitalwert = 0 wird
- Risikobetrachtung statt Wertbetrachtung: [[Dynamische Amortisationsrechnung]]
- Statische Vereinfachung: [[Gewinnvergleichsrechnung]]

## Lernkarten

Q: Was ist die Kapitalwertmethode?
A: Ein **dynamisches** Investitionsrechenverfahren, das den Barwert aller zukünftigen Ein- und Auszahlungen einer Investition ermittelt, abgezinst auf den Zeitpunkt $t_0$.

Q: Wie lautet die Formel des Kapitalwerts?
A: $$KW = \sum_{t=0}^{n} \frac{Z_t}{(1+i)^t} = -A_0 + \sum_{t=1}^{n} \frac{Z_t}{(1+i)^t}$$

Q: Wann ist eine Investition nach der Kapitalwertmethode vorteilhaft?
A: Bei einer **Einzelentscheidung**: wenn $KW > 0$ (die Investition erwirtschaftet mehr als die geforderte Mindestverzinsung). Bei einer **Auswahlentscheidung**: die Alternative mit dem höchsten positiven Kapitalwert wählen.

Q: Was bedeutet ein Kapitalwert von genau 0?
A: Die Investition erwirtschaftet **genau die Mindestverzinsung**. Der verwendete Zinssatz entspricht dann dem internen Zinsfuß.

Q: Nenne zwei Vorteile und zwei Nachteile der Kapitalwertmethode.
A: **Vorteile:** Theoretisch fundiert (berücksichtigt Zeitwert des Geldes), eindeutiges Ergebnis ohne Mehrdeutigkeit.
**Nachteile:** Abhängig vom gewählten Kalkulationszins, zukünftige Zahlungen müssen geschätzt werden.

Q: Das ist ein Test
A: **Vorteile:** Testantwort
**Nachteile:** Nachteil Test
