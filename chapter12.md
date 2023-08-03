---
recall: header
---

### Womit beschäftigt sich die Chaostheorie?

Untersuchung nichtlinearer dynamischer Systeme

### Was ist die Aufgabe der Chaostheorie?

in scheinbar regellosem (chaotischem) Verhalten von Systemen Strukturen zu entdecken

### Was sind zwei wesentliche Merkmale von chaotischen Systemen?

- Bifurkationen
- seltsame Attraktoren

### Was bedeutet es, wenn ein System sich "chaotisch" verhält?

- deterministisch (wiederholbare Ergebnisse mit gleich Anfangsbedingungen)
- sehr empfindlich auf Änderungen der Anfangsbedingungen

### Wie werden diskrete Systeme noch genannt?

Iterationsfunktionen

### Wie viele Zustandsvariablen sind bei einem kontinuierlichen System für chaotisches Verhalten mindestens nötig?

drei

### Was ist eine Iterationsfunktion?

eine Funktion zur Berechnung des Zustands eines Systems, bei der der Zustand zum nächsten Zeitpunkt aus dem vorherigen iterativ berechnet wird

### Was ist ein Fixpunkt einer Iterationsfunktion?

ein Zustand der sich bei Anwendung der Iterationsfunktion nicht ändert

### Was ist ein anziehender Fixpunkt?

ein Zustand zu dem ein System aus mehreren Startzuständen (in der Umgebung) strebt

### Wie kann ein anziehender Fixpunkt identifiziert werden?

der Betrag der erste Ableitung der Iterationsfunktion ist kleiner als 1

### Wie kann ein abstoßender Fixpunkt identifiziert werden?

der Betrag der erste Ableitung der Iterationsfunktion ist größer als 1

### Wie wird der zeitliche Abschnitt der Systemdynamik bis zum Erreichen eines Fixpunktes genannt?

transiente Dynamik

### Was ist "asymptotischen Dynamik" eines Systems?

Konvergiert ein System gegen einen Fixpunkt, verschwindet die transiente Dynamik und das System geht in ein stationäres Verhalten, die asymptotische Dynamik über. Zyklen und seltsame Attraktoren passen besser zum Begriff, da das System bei diesen noch eine echte Dynamik aufweist.

### Was ist die logistische Abbildung?

eine eindimensionale Iterationsfunktion, die zur Modellierung von Populationswachstum verwendet wird
$$
\Phi(x) = rx(1-x)
$$

### Was ist eine Bifurkation?

qualitative Zustandsänderung in nichtlinearen Systemen bei Änderung eines Systemparameters

### Was ist eine transkritische Bifurkation?

tauschen bei Variation eines Systemparameters zwei Fixpunkte ihr Stabilitätsverhalten, ist das eine transkritische Bifurkation

### Wie konstruiert man die grafische Iteration einer Iterationsfunktion?

- Graph mit $x_n$ auf x-Achse und $x_{n+1}$ auf y-Achse
- Iterationsfunktion einzeichnen
- Ursprungsgerade mit Steigung 1 einzeichnen
- Startpunkt auf Diagonale eintragen
- vertikale durch Startpunkt mit Iterationsfunktion verschneiden
- horizontale vom Schnittpunkt zur Diagonalen gibt nächsten Funktionswert

### Was ist eine "superkritische Gabelbifurkation"?

das Systemverhalten ändert sich von der Existenz eines Fixpunktes, gegen den das System konvergiert, zu zwei Punkten zwischen denen das System oszilliert

### Warum ist die superkritische Gabelbifurkation "harmlos"?

zwar ändert sich das Systemverhalten, allerdings führt eine leichte Änderung des Systemparameters auch nur zu einer leichten Änderung des verhaltens, weil die beiden Oszillationspunkte aus dem vorherigen Fixpunkt entstehen und sich erst mit weiter wachsendem Systemparameter davon weg bewegen

### Was ist eine "subkritische Gabelbifurkation"?

das Systemverhalten ändert sich von der Existenz eines Fixpunktes, gegen den das System konvergiert, zu einem chaotischen Verhalten ohne Fixpunkte oder Oszillation

### Warum ist die subkritische Gabelbifurkation kritisch?

weil sich das Systemverhalten bei Übergang des Bifurkationspunktes unerwartet verhält und kleine Änderungen zu extremen Antworten des Systems führen können

### Wie kann das asymptotische Verhalten einer Iterationsfunktion simuliert werden?

mehrere hundert (oder mehr) Schritte simulieren, bis das transiente Verhalten abgeklungen ist, die danach auftretenden Zustände visualisieren

### Was ist ein Bifurkationsdiagramm?

eine grafische Darstellung des asymptotischen Verhaltens eines Systems über einem Systemparameter

### Wie wird ein Bifurkationsdiagramm erzeugt?

- mehrfache Simulation des System mit variiertem Parameter
- Darstellung der asymptotischen Dynamik in jeder "Spalte" des Plots

### Was zählt zu den klassischen Attraktoren?

- Fixpunkte
- stabile Zyklen

### Was ist ein seltsamer Attraktor?

- Systemzustand bewegt sich in beschränktem Gebiet
- manche Bereiche des Systemzustands werden häufiger eingenommen als andere

### Wann spricht man im Bifurkationsdiagramm von chaotischem Verhalten?

wenn keine Periodizität des Systemzustands mehr erkennbar ist

### Wie nennt man es, dass man im Bifurkationsdiagramm Teilbereiche findet, die wie das Bifurkationsdiagramm selbst aussehen?

Selbstähnlichkeit

### Wie lautet die Definition eines allgemeinen Attraktors?

kleinsmögliche Menge von Zuständen aus dem Zustandsraum eines dynamischen Systems, die von allen Startzuständen erreicht wird und im stationären Verhalten des Systems nicht verlassen wird

### Was ist die Cantor-Menge?

eine Teilmenge der rellen Zahlen des Intervalls $[0,1]$ die konstruiert wird, indem ausgehend von allen Zahlen des Intervall wiederholt das mittlere Drittel der noch vorhandenen Intervalle unendlich oft entfernt wird

### Wie wird die fraktale Dimension insbesondere selbstähnlicher Figuren bestimmt?

Skaliert man eine einfache Figur und einen ganzzahligen Faktor, besteht die neue Figur aus n Kopien
(Vergrößerung) bzw. passt n mal in die Ausgangsfigur (Verkleinerung). Die Anzahl n ergibt sich aus
$\text{Skalierungsfaktor}^\text{Dimension}$

### Wie ergibt sich die fraktale Dimension der Cantor-Menge?

Wie die Länge der Ausgangslinie verdreifacht, ergeben sich nach dem ersten Löschen des mittleren
Drittels zwei Linien der Länge 1, genau der Ausgangslinie der unskalierten Cantor-Menge. Bei einem Skalierungsfaktor von 3, ergeben sich also zwei Cantor-Mengen.

$$
\text{Anzahl Kopien} = \text{Skalierungsfaktor}^\text{Dimension}
$$

Also 

$$
\text{Dimension} = \frac{\ln \text{Anzahl Kopien}}{\ln \text{Skalierungsfaktor}} = \frac{\ln 2}{\ln 3} = 0.63093
$$

### Wie lautet die Definition eines seltsamen Attraktors?

- allgemeiner Attraktor
- chaotisches Verhalten, ähnliche Startwerte entfernen sich voneinander
- fraktale Dimension

### Was ist die "Hénon-Abbildung"?

eine nichtlineare, zweidimensionale Abbildung, die einen seltsamen Attraktor besitzt

### Wie verhält sich die Modellierungsmethode dynamischer Systeme zur Anzahl Iterationen bis zur asymptotischen Dynamik?

- eindimensionale diskrete Systeme benötigen am wenigsten Iterationen
- mehrdimensionale diskrete Systeme schon Tausende bis Millionen Iterationen
- kontinuierliche Systeme benötigen am längsten, bis Attraktoren erreicht werden

### Wozu dient der Poincaré-Schnitt?

eine Methode ein kontinuierliches System um eine Dimension zu reduzieren

### Wie wird der Poincaré-Schnitt gebildet?

in einem n-dimensionalen Phasenraum, wird eine (n-1)-dimensionale Struktur plaziert und die Schnitte mit der Zustandstrajektorie (von der immer gleichen Seite) aufgenommen

### Wie ist die Periode eines kontinuierlichen dymanischen Systems definiert?

Anzahl der Punkte im Poincaré-Schnitt
