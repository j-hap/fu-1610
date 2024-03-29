---
recall: header
---

### Was ist der Zustandsraum der Populationsdynamik?

Anzahl von Individuen (kontinuierlich, da einfacher zu handhaben als diskrete Werte)

### Auf welcher Basis werden kontinuierliche Modelle der Populationsdynamik modelliert?

Differentialgleichungen

### Welche Raten sind für das Ein-Spezies-Modell von Malthus entscheidend?

- Geburtenrate $\gamma$
- Sterberate $\delta$
- Wachstumsrate $\lambda$ (als Differenz von Geburten- und Sterberate)

### Was bedeutet "lineares Modell" im Kontext der Populationsdynamik?

Wachstum der Population (Ableitung) wird linear in Abhängigkeit der Populationsgröße modelliert,
ergibt aber eine exponentielle Gleichung der Population über der Zeit

### Wie lautet die Differentialgleichung des linearen Modells der Populationsdynamik?

$$ \dot{p}(t) = \lambda p(t) $$

### Für welches Modell ist der Mathematiker Pierre-François Verhulst bekannt?

- linearen Modells mit Sättigung der Populationsdynamik
- logistische Abbildung

### Wie lautet die Differentialgleichung des linearen Modells mit Sättigung der Populationsdynamik?

$$ \dot{p}(t) = \lambda_0 - \lambda_1 p(t) $$

### Welchen Nachteil haben lineare Modelle der Populationsdynamik?

es lässt sich entweder ein exponentielles Wachstum oder eine Abnahme der Populationsänderung für
große Populationen modellieren, aber nicht beides

### Was bedeutet "logistisches Modell" im Kontext der Populationsdynamik?

ein Modellansatz der Populationsdynamik, in der die Wachstumsrate $\lambda$ linear von der
Populationsgröße abhängt und die Populationsänderung von der Wachstumsrate und der Populationsgröße,
also damit quadratisch von der Populationsgröße

### Wie lautet die logistische Differentialgleichung der Populationsdynamik?

$$ \dot{p}(t) = \lambda(p(t)) \cdot p(t) = (a-b \cdot p(t)) \cdot p(t) = ap(t) - bp(t)^2 $$

### Was ist ein Gleichgewichtspunkt in der Populationsdynamik?

eine Populationsgröße, bei der die Änderung der Population auf 0 sinkt  
allgemeiner: ein Fixpunkt

### Wie viele Gleichgewichtspunkte hat das logistische Modell der Populationsdynamik?

zwei

### Wo liegt das stabile Gleichgewicht der logistischen Differentialgleichung?

Aus 
$$ \dot{p}(t) = a \overline{p} - b  \overline{p} ^2 = (a - b \overline{p}) \overline{p} = 0 $$
folgt
$$ \overline{p} = 0 $$
und
$$ \overline{p} = \frac{a}{b} $$

### Welche Anwendungsfälle gibt es für Zwei-Spezies-Modelle?

- Kampf um Ressourcen (gleiche Nahrungsquelle)
- Räuber-Beute-Modelle

### Welche Konsequenz hat ein Aussterben der Beute im Zwei-Spezies-Modell für den Räuber?

Gemäß dem Modell stirbt auch der Räuber aus. Hat der Räuber auch andere Nahrungsquellen oder kann
andere Populationen der Beute aufsuchen, stößt das Modell an die Grenzen, weil der Räuber in der
Realität nicht ausstirbt

### Wie sind Gleichgewichtspunkte im Zwei-Spezies-Modell charakterisiert?

beide Wachstumsraten verschwinden

### Wie verhält sich das Zwei-Spezies-Modell wenn eine der Populationen verschwindet?

wie das logistische Ein-Spezies-Modell

### Wie kann man Räuber-Beute-Modelle an den Parametern erkennen?

eine große Population von P beschleunigt das Wachstum von Q (positives Vorzeichen) aber eine große
Population von Q beschränkt das Wachstum von P (negatives Vorzeichen) (oder andersherum)

### Wie kann man Konkurrenz-Modelle an den Parametern erkennen?

die Größe der jeweils anderen Population beschränkt das Wachstum (negatives Vorzeichen)

### Was bedeuten negative, reellwertige Eigenwerte der Jakobi-Matrix im Zwei-Spezies-Modell?

attraktiver Gleichgewichtpunkt

### Was bedeuten rein imaginäre Eigenwerte der Jakobi-Matrix im Zwei-Spezies-Modell?

abstoßender Gleichgewichtspunkt (Oszillation ums Gleichgewicht)

### Was ist die Lösung eines diskreten Ein-Spezies-Modell?

ein zeitlicher Verlauf der Verteilungsfunktion der stochastischen Populationsgröße

### Was ist das SIR-Modell?

ein klassischer Ansatz zur Beschreibung der Ausbreitung von ansteckenden Krankheiten mit
Immunitätsbildung

### Wofür steht SIR?

susceptible-infected-removed

