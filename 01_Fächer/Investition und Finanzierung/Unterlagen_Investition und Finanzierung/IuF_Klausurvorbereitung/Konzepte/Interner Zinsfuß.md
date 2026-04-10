# Interner Zinsfuß

#konzept #investitionsrechnung #dynamisch

## Definition
Der interne Zinsfuß (auch: Internal Rate of Return, IRR) ist derjenige Zinssatz $r$, bei dem der [[Kapitalwertmethode|Kapitalwert]] einer Investition exakt Null wird. Er gibt die **effektive Maximalverzinsung** des gebundenen Kapitals an.

## Einordnung
Gehört zu den **dynamischen Verfahren** (wie [[Kapitalwertmethode]], [[Dynamische Amortisationsrechnung]], [[Annuitätenmethode]]). Berücksichtigt den Zeitwert des Geldes.

## Formel

Der interne Zinsfuß $r$ ist die Lösung der Gleichung:

$$KW = \sum_{t=0}^{n} \frac{Z_t}{(1+r)^t} = 0$$

### Sonderfälle (In der Klausur erkennbar!)

| Zahlungsreihentyp | Erkennung | Lösung |
|---|---|---|
| **Kuponanleihe** | Gleiche Zahlungen + Rückzahlung am Ende | $r = \frac{Kupon}{Investition}$ (Kopfrechnen!) |
| **Zerobond** | Nur Anfangs- und Endzahlung | $r = \sqrt[n]{\frac{Endwert}{Investition}} - 1$ |
| **Allgemein** | Unregelmäßige Zahlungsreihe | Regula Falsi / Iteration nötig |

## Entscheidungsregel
- **Einzelentscheidung:** Investition vorteilhaft, wenn $r > i$ (Kalkulationszins)
- **Auswahlentscheidung:** Wähle die Alternative mit dem **höchsten internen Zinsfuß** (bei gleicher Anfangsauszahlung und Laufzeit)

## ⚠️ Probleme der Methode
- Bei nicht-normalen Zahlungsreihen (Vorzeichenwechsel > 1) können **mehrere interne Zinsfüße** existieren
- Einmal-Investitionen mit unterschiedlichen Volumina sind schlecht vergleichbar (Wiederanlageprämisse)

## Zusammenhänge
- Der Kapitalwert bei Zinssatz $r$ ist per Definition 0: Siehe [[Kapitalwertmethode]]
- Risikobasierte Alternative: [[Dynamische Amortisationsrechnung]]
- Rechenbeispiel siehe [[KV IuF Aufgaben|Übungsblock 2, Aufgabe 3]]
