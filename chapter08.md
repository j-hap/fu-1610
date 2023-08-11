---
recall: header
---

### Was ist mikroskopische Verkehrsimulation?

die Simulation von Straßenverkehr durch Abbildung jedes einzelnen Verkehrsteilnehmers

### Was zeichnet makroskopische Verkehrsimulation aus?

kollektive Gesamtdynamik wird auf Basis der Simulation aller individuellen Verkehrteilnehmer
ermittelt

### Wie unterscheiden sich makroskopische und mikroskopische Verkehrssimulation in Bezug auf Überholmanöver?

bei makroskopischer Simulation implizit die Möglichkeit dazu gegeben, bei mikroskopischer nicht.

### Was sind "Fahrzeug-Folge-Modelle"?

erste Ansätze zur mikroskopischen Modellierung, bei denen jeder Verkehrsteilnehmer über partielle
Differentialgleichung modelliert wird

### Was ist das "Nagel-Schreckenberg Modell"?

Modellansatz zur mikroskopischen Verkehrssimulation auf Basis von zellulären Automaten

### Was sind "zellulären Automaten"?

ein Modellansatz für räumlich diskretisierter dynamischer Systeme, wobei der Folgezustand einer
Zelle vom eigenen und dem Zustand der Nachbarzellen abhängt

### Wer entwickelte die Theorie der zellulären Automaten?

Stanislav Ulm

### Was sind die fünf Grundcharakteristika von zellulären Automaten?

- Zellraum: Menge ein- oder zweidimensionaler Zellen gleicher geometrischer Form
- Zustandsmenge: jede Zelle kann einen (diskreten) Zustand einer Zustandsmenge annehmen
- Nachbarschaftsbeziehung: jede Zelle kennt benachbarte Zellen. Diese beeinflussen sich gegenseitig.
- diskrete Zeit: Zustand des der Zellen im Automaten ändert sich in diskreten Zeitschritten
- Lokale übergangsfunktion: Nur der eigene Zustand und der der benachbarten Zellen beeinflusst den
  Übergang in einen neuen Zustand.

### Welche Zellformen werden bei zweidimensionalen zellulären Automaten für gewöhnlich verwendet?

- rechteckig
- hexagonal (sechseckig)
- dreieckig

### Welche Nachbarschaftsbeziehungen gibt es bei zellulären Automaten mit rechteckigen Zellen?

- Moore-Nachbarschaft: Zellen, die sich eine Kante teilen sind benachbart
- von-Neumann-Nachbarschaft: Zellen, die sich mindestens eine Ecke teilen sind benachtbart

### In welcher Reihenfolge wird der Folgezustand von Zellen in einem zellulären Automaten berechnet?

Der neue Zustand wird für alle Zellen parallel berechnet.

### Was ist die bekannteste Anwendung von zellulären Automaten?

John Conway - Game Of Life (1970)

### Was ist ein "kartesischer zellulärer Automat"?

ein zweidimensionaler zellulärer Automat mit rechteckigen Zellen

### Welche Nachbarschaftsbeziehung kommt beim "Game Of Life" zum Einsatz?

Moore-Nachbarschaft (gemeinsame Kante)

### Was sind die drei Regeln des "Game Of Life"

1. lebende Zelle mit <2 oder >3 lebenden Nachbarn stirb
2. lebende Zelle mit 2 oder 3 lebenden Nachbarn lebt weiter
3. tote Zelle mit genau 3 Nachbarn wird lebendig

(genau genommen sind Regeln 1 und 2 redundant)

### Was ist eine Zelle im Nagel-Schreckenberg-Modell?

ein eindimensionaler Fahrbahnabschnitt fester Länge

### Was ist der Zustand einer Zelle im Nagel-Schreckenberg-Modell?

mögliche Zustände:
- kein Auto
- Auto mit Geschwindigkeit x

### Wie wird die Geschwindigkeit eines Fahrzeugs im Nagel-Schreckenberg-Modell angegeben?

Zellen / Zeitschritt

### Warum erlaubt das Nagel-Schreckenberg-Modell nur diskrete Geschwindigkeiten?

Damit Fahrzeuge sich nach einem Zeitschritt nicht zwischen zwei Zellen befinden

### Welcher funktionale Zusammenhang besteht zwischen der maximalen Geschwindigkeit, der Zeitschrittweite und der Zellgröße im Nagel-Schreckenberg-Modell?

$$\tilde{v}_{max} = \frac{v_{max} \cdot L_{Zelle}}{\Delta t} $$
  
wobei $\tilde{v}_{max}$ die Geschwindigkeit in $\frac{\mathrm{km}}{\mathrm{h}}$ und $v_{max}$ die maximale Geschwindigkeit in Zellen pro Zeiteinheit beschreibt

### Was sind zentrale Modellannahmen im Nagel-Schreckenberg-Modell?

1. Kollisionsfreiheit
2. Erhaltung der Fahrzeuge

### Was bedeutet Kollisionsfreiheit in der mikroskopischen Verkehrssimulation?

zwei Fahrzeuge dürfen innerhalb eines Zeitschritts nie dieselbe Zelle befahren

### Wie ist der Abstand zwischen zwei Fahrzeugen im Nagel-Schreckenberg-Modell definiert?

Anzahl der freien Zellen zwischen zwei Fahrzeugen

### Wie lautet der Algorithmus zur Berechnung des nächsten Zeitschritts im Nagel-Schreckenberg-Modell?

Für alle Fahrzeuge parallel:
1. Beschleunigen: $v_i = \min \lbrace v_i+1, v_{max}\rbrace$
2. Bremsen: $v_i = \min \lbrace v_i, d(i, i+1) \rbrace$, wobei $d(i, j)$ der Abstand zum Vordermann ist
3. Bewegen: jedes Fahrzeug $i$ bewegt sich $v_i$ Zellen vorwärts

### Was ist eine "periodische Randbedingung"?

bei einem begrenzen Simulationsgebiet werden gegenüberliegende Ränder gekoppelt. In der
Verkehrssimulation bedeutet das, das Fahrzeuge, die das Simulationsgebiet am rechten Rand verlassen
am linken Rand mit gleicher Geschwindigkeit wieder auftauchen

### Was ist die "kritische Dichte" im Nagel-Schreckenberg-Modell?

die Fahrzeugdichte, bei der alle Fahrzeuge gerade genau ihre Zelle + $v_{max}$ Zellen vor sich zur
Verfügung haben, um auf Maximalgeschwindigkeit zu beschleunigen (bei $\tilde{v}_{max} =
\frac{v_{max} \cdot L}{\Delta t}$), bei kritischer Dichte herrscht maximaler Fluss

### Wozu führt ein Überschreiten der kritischen Dichte im Nagel-Schreckenberg-Modell?

Stau

### Was ist der "Trödelfaktor" im Nagel-Schreckenberg-Modell?

stochastische Erweiterung, die Fahrzeuge zufällig um 1 von der Maximalgeschwindigkeit abbremsen
lässt oder um 1 zu stark abbremsen lässt

### Was repräsentiert der Trödelfaktor im im Nagel-Schreckenberg-Modell?

- Überreagieren von Fahrern bei Bremsvorgängen
- zu wenig Gas bei Fahrern ohne Tempomat, um die Geschwindigkeit zu halten (Anstieg, Gegenwind)
- Verzögerung beim Beschleunigen, wenn Straße frei wird

### Wie wird der Tödelfaktor im Algorithmus zur Berechnung des nächsten Zeitschritts im Nagel-Schreckenberg-Modell eingefügt?

Zwischen Bremsen und Bewegen wird der Punkt  
Trödeln: $v_i = \max \lbrace v_i - 1, 0 \rbrace$ mit Wahrscheinlichkeit $0 < p < 1$  
eingefügt.

### Mit welcher Durchschnittsgeschwindigkeit bewegen sich die Fahrzeuge im Nagel-Schreckenberg-Modell mit Trödelfaktor in der Freiflussphase?

$$
\overline{\tilde{v}} = \frac{(v_{max} -p) \cdot L_{Zelle}}{\Delta t}
$$

### Wie hoch ist der maximale Fluss im Nagel-Schreckenberg-Modell?

bei kritischer Dichte und damit maximaler Geschwindigkeit aller Fahrzeuge ist der maximale Fluss
$$
f_{max} = \frac{v}{v+1} \frac{\mathrm{Fzg}}{{s}}
$$

### Woraus besteht ein Verkehrsgraph?

- Knoten: Alles, was den Verkehrsfluss ändert, Kreuzungen, Geschwindigkeitsbeschränkungen,
  Ausfahrten, ...  
- gerichtete Kanten: Straßenabschnitte mit konstanten Bedingungen, gewichtet mit der Länge der
  Straßenabschnitts

### In welche drei Kategorien lassen sich Kreuzungen einordnen?

- ungeregelt (recht-vor-links)
- geregelt (Schilder / Ampeln)
- Kreisverkehr

### Was sind "Deadlocks" bei der Modellierung von Kreuzungen?

in der Realität eher selten eintretender Fall, dass an einer ungeregelten Kreuzung aus allen
Richtungen ein Fahrzeug wartet

### Was ist das "Vier-Phasen-Modell" bei der Modellierung von Kreuzungen?

- einfache Modellierung zur Regelung von Vorfahrt an ungeregelten Kreuzungen
- Deadlocks werden vermieden
- Verkehrteilnehmer müssen nur die eigene Abbiegepräferenz berücksichtigen
- imitiert Ampelschaltung mit Grünphase für Linksabbieger

### Wie werden Kreisverkehre im Nagel-Schreckenberg-Modell modelliert?

zirkuläre Streckenabschnitte mit Abzweigungen nach rechts

### Wie kann eine ungeregelte Kreuzung im Nagel-Schreckenberg-Modell modelliert werden, um einen Deadlock zu vermeiden?

- Vier-Phasen-Modell
- Mini-Kreisverkehr

### Wann kommt das Vier-Phasen-Modell typischerweise zum Einsatz?

Modellierung von unkritischen Kreuzungen in Wohngebieten, weil es zu realitätsfern ist

### Wie wird in der Simulation entschieden welches Fahrzeug welche Abbiegung nimmt?

gleichverteilte Wahrscheinlichkeiten sind unrealistisch, weil Hauptstraßen dann zu wenig befahren
werden, Entscheidungen sollte auf Beobachtungen des realen Verkehrs basieren

### Was sind "Multi-Agenten-Simulationen"?

Fahrzeuge werden als autonom handelnder Agent betrachtet mit individueller
- Höchstgeschwindigkeit
- Trödelfaktor
- Fahrzeuggröße
- Verhaltensmuster

### Was sind "Origin-Destination-Matrizen" (OD-Matrizen)?

Matrix die zu jedem Start-Punkt (Origin) und Ziel-Punkt (Destination) angibt mit welcher
Wahrscheinlichkeit diese Kombination auftritt. Entsprechend häufig werden Fahrzeuge an diesen
Startpunkten mit diesem Ziel erstellt. Wahrscheinlichkeiten stammen aus Befragungen und
Beobachtungen

### Wie funktioniert der Dijkstra-Algorithmus zur Suche nach der kürzesten Route zwischen zwei Knoten?

0. Startknoten mit Gesamtkosten 0 in die Menge der Randknoten $R$ einfügen Solang R noch nicht leer:  
1. Knoten mit geringsten Gesamtkosten aus R entnehmen und zum aktiven Knoten $a$ machen, zur Menge
   Besuchter Knoten $B$ hinzufügen. Ist es der Zielknoten, abbrechen
2. Gesamtkosten aller Nachbarn von $a$ über $a$ berechnen: Gesamtkosten von $a$ + Kantengewicht von
   $a$ zum Nachbarn
   - Nachbar schon in R: wenn neue Kosten geringer als eingetragene, neue Kosten übernehmen und $a$
     als Vorgänger eintragen
   - Nachbar noch nicht in R: Nachbar in $R$ aufnehmen, Gesamtkosten zu berechneten ersetzen und
    $a$ als Vorgänger eintragen

### Welche Laufzeitkomplexität hat der Dijkstra-Algorithmus?

- $\mathcal{O}(\vert V \vert ^2 + \vert E \vert)$ bei verketteter Liste / Array für $R$
- $\mathcal{O}(\vert V \vert \cdot \log(V) + \vert E \vert)$ mit Fibbonaci-Heap für $R$

### Welcher Zusammenhang zwischen Knoten- und Kantenanzahl kann in Verkehrsnetzen angenommen werden?

$\mathcal{O}(\vert E \vert) = \mathcal{O}(\vert V \vert)$

### Was ist ein guter Richtwert für das Verhältnis der Anzahl Kanten zur Anzahl Knoten in einem Verkehrsnetz?

$3:1$

### Welchen Nachteil hat der Dijkstra-Algorithmus bei der Routenplanung?

sucht uninformiert durch den Graphen ohne die Richtung des Ziels mit einzubeziehen

### Was ist der $A^*$-Algorithmus?

Erweiterung des Dijkstra Algorithmus um eine Heuristik, die die Restkosten zum Ziel für Randknoten
abschätzen kann

### Was zeichnet eine zulässige Heuristik beim $A^*$-Algorithmus aus?

- Überschätzt nie die Kosten bis zum Ziel
- Monoton

### Welche Heuristik kommt bei der Routenplanung mit dem $A^*$-Algorithmus zur Routenplanung zum Einsatz?

Luftliniendistanz

### Was ist eine "Ganglinie"?

Ganglinie zeigt in Abhängigkeit von der Tageszeit für jede volle Stunde, welcher Anteil der
Verkehrsteilnehmer im Verkehrsnetz ihre Fahrt beginnen

### Wie können realistische Szenarien wie die "Rush-Hour" im Nagel-Schreckenberg-Modell abgebildet werden?

durch OD-Matrizen in Verbindung mit Ganglinien

### Was versteht man unter inhomogenen Verkehrsteilnehmern?

Vergleichbar mit Multi-Agenten-Simulationen, wenn nicht alle Verkehrsteilnehmer die gleiche Fahrzeuglänge, Trödelfaktor und Höchstgeschwindigkeit haben

### Was sind Beispiele für inhomogene Modellverfeinerungen im Nagel-Schreckenberg-Modell?

- LKW / Traktor: Länger als eine Zelle, geringe Höchstgeschwindigkeit
- Motorräder / Fahrräder: Können nebeneinander fahren
- Sonntagsfahrer: Hoher Trödelfaktor

### Welche Erweiterung wird durch die Modellierung inhomogenen Verkehrsteilnehmer erwungen?

Überholvorgänge, weil sich sonst der Verkehr hinter den Langsamen staut

### Wie fein werden Zellen im im Nagel-Schreckenberg-Modell aktuell modelliert?

$\leq 30 \thinspace \mathrm{cm}$

### Wie lässt sich die Modellierung des Trödelfaktors verfeinern?

höhere Wahrscheinlichkeiten für Trödeln beim Anfahren und Beschleunigen als beim Abbremsen
