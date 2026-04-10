### Signale: Analog vs. Digital

| Typ | Beschreibung | Verwendung |
|---|---|---|
| **Analog** | Kontinuierliche Spannungs-/Frequenzänderung, z. B. Sinuswellen | Funk, alte Telefonsysteme |
| **Digital** | Diskrete Werte (0/1), rechteckige Impulsfolgen | Computerkommunikation |

### Fourier-Analyse

Jedes periodische Signal = Summe von Sinus- und Kosinuswellen (Harmonische).
- Zeigt, wie viel **Bandbreite** ein Signal benötigt
- Rechtecksignal → unendlich viele Frequenzanteile → in der Praxis: Begrenzung

### Bandbreite

Bereich der Frequenzen, die ein Kanal übertragen kann (z. B. 3 kHz bis 3 MHz).
Beschränkt die maximal übertragbare Informationsmenge.

### Grenzen der Datenübertragung

**Nyquist-Grenze** (rauschfreier Kanal):
```
maximale Datenrate = 2 · B · log₂(V)
```
- B = Bandbreite (Hz), V = Anzahl diskreter Signalwerte

**Shannon-Grenze** (verrauschter Kanal):
```
maximale Datenrate = B · log₂(1 + S/N)
```
- S/N = Signal-Rausch-Verhältnis (linear, nicht in dB)

| Begriff | Bedeutung |
|---|---|
| **Nyquist** | Max. Datenrate ohne Rauschen |
| **Shannon** | Theoretisches Maximum mit Rauschen |
| **S/N-Verhältnis** | Signalstärke zu Rauschleistung |

> **Merksatz:** Je breiter der Kanal und je besser das Signal, desto mehr Daten passen hindurch – aber physikalische Grenzen bleiben.

→ Siehe auch: [[Übertragungsmedien]] | [[Drahtlose Übertragung]] | [[OSI- und TCP-IP-Modell]]

## Lernkarten

Q: Was besagt die Nyquist-Formel?
A: Maximale Datenrate (rauschfreier Kanal) = **2 · B · log₂(V)** – mit B = Bandbreite (Hz), V = Anzahl diskreter Signalwerte.

Q: Was besagt die Shannon-Formel?
A: Maximale Datenrate (verrauschter Kanal) = **B · log₂(1 + S/N)** – mit B = Bandbreite (Hz), S/N = Signal-Rausch-Verhältnis (linear).

Q: Was ist der Unterschied zwischen Nyquist- und Shannon-Grenze?
A: **Nyquist**: gilt für rauschfreie Kanäle, berücksichtigt diskrete Signalwerte. **Shannon**: gilt für verrauschte Kanäle, berücksichtigt das Signal-Rausch-Verhältnis – gibt das theoretische Maximum an.

Q: Was ist Fourier-Analyse im Kontext der Datenübertragung?
A: Jedes periodische Signal lässt sich in eine Summe von Sinus- und Kosinuswellen zerlegen. Dies zeigt, wie viel **Bandbreite** ein Signal benötigt und wie es sich durch Filter verändert.
