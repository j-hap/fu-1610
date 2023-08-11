---
recall: header
---

### Worum geht es beim Prozess der Erstellung von Zeitplänen?

- Optimale Ausnutzung von Ressourcen
- Berücksichtigung von Abhängigkeiten / Reihenfolgen
- Berücksichtigung von Kapazitäten

### Was ist deterministisches Prozess-Scheduling?

Festlegen von auf Basis eines Kostenmaßes optimalen Bearbeitungszeiten von Aufträgen bei bekannter
Auftragsdauer

### Was ist der hauptsächliche Anwendungsfall für Prozess-Scheduling in der Informatik?

Festlegen einer Bearbeitungsreihenfolge für I/O und CPU Jobs

### Was ist ein zulässiger Zeitplan?

ein Zeitplan, der alle Anforderungen bezüglich Bearbeitungsreihenfolge, Maschinenkapazitäten, etc.
einhält.

### Welches Kriterium wird für die Bewertung von Zeitplänen genutzt?

Kostenmaß wie zum Beispiel Gesamtkosten oder Gesamtdauer

### Was ist eine "Präzedenzbedingung"?

Eine Präzedenzbedingung zwischen den Aufträgen $A_i, A_j$ besagt, dass $A_i$ fertig bearbeitet sein
muss, bevor $A_j$ begonnen wird.

### Wie werden Präzedenzbedingungen notiert?

Bei den Aufträgen $A_i, A_j$ besagt $A_i \rightarrow A_j$, dass $A_i$ fertig bearbeitet sein muss,
bevor $A_j$ begonnen wird.

### Wie werden Präzedenzbedingungen in einem Graphen berücksichtigt?

Jede Präzedenzbedingungen führt zu einer Kante im Graphen.

### Was ist ein "Präzedenzgraph"?

Ein Graph mit Aufträgen als Knoten, wobei Aufträge, die vor einem anderen erledigt werden müssen mit
einer gerichteten Kante zum Nachfolger mit diesem verbunden sind.

### Welche Knoten werden im Präzedenzgraphen eingetragen?

- ein Knoten pro Auftrag (enthält Name und Bearbeitungszeit)
- Startknoten (Bearbeitungszeit 0)
- Endknoten (Bearbeitungszeit 0)

### Was zeichnet den Startknoten $A_S$ im Präzedenzgraphen aus?

- Bearbeitungszeit 0
- Präzedenzbedingung zu allen Bearbeitungsschritten ($A_S \rightarrow A_i$)
- Startzeit $s_S = 0$;

### Was zeichnet den Startknoten $A_E$ im Präzedenzgraphen aus?

- Bearbeitungszeit 0
- Präzedenzbedingung zu allen Bearbeitungsschritten ($A_i \rightarrow A_E$)

### Was ist die "makespan" eines Jobs?

Gesamtfertigungszeit

### Wie wird der Startknoten im Präzedenzgraphen bezeichnet?

$A_S$ bzw. $A_0$

### Wie wird der Endknoten im Präzedenzgraphen bezeichnet?

$A_E$ bzw. $A_{n+1}$

### Was bedeutet ein Zyklus im Graphen für Prozess-Scheduling?

dass es keinen zulässigen Zeitplan gibt

### Wofür steht die Abkürzung DAG?

directect acyclic graph - gerichteter, kreisfreier Graph

### Wann ist ein DAG topologisch sortiert?

wenn der Ausgangsknoten jeder Kante eine geringere Nummer hat als der Zielknoten

### Mit welchem Algorithmus lässt sich ein DAG topologisch sortieren?

Tiefensuche

### Was ist die "Vorlaufzeit" eines Auftrags?

Zeitdauer zwischen Beginn des Prozesses und frühestem Beginn des Auftrags

### Wie werden Vorlaufzeit und Fertigstellungszeit notiert?

$s_i'$ und $c_i'$

### Wann ist ein Knoten im Graphen für Prozess-Scheduling kritisch?

wenn frühest- und spätestmögliche Startzeit für den Auftrag identisch sind

### Was zeichnet einen kritischen Pfad beim Prozess-Scheduling aus?

Er enthält ausschließlich kritische Knoten.

### Was ist Schlumpf beim Prozess-Scheduling?

die Differenz zwischen spätest- und frühestmöglicher Startzeit eines Knotens

### Wie ergibt sich die Gesamtfertigungszeit eines Prozesses?

länge des kritischen Pfades im zugehörigen Graphen

### Was ist die "Kritischer-Pfad-Methode"?

Optimierung eines Zeitplans über Identifikation kritischer Pfade

### Welche Diagramme kommen typischerweise bei  der "Kritischer-Pfad-Methode" zum Einsatz?

- Gannt-Diagramme
- Netzpläne

### Welche Nachteile hat das Kostenmaß Gesamtfertigungszeit?

- berücksichtigt nicht, dass ein möglichst später Start die Lagerhaltung reduziert
- berücksichtigt nicht, dass ein möglichst früher Start Sicherheit für eventuell eintretende
  Probleme schafft ohne den Liefertermin zu verletzen

### Wofür kann Schlupf verwendet werden?

Ausgleich von Verzögerungen von früheren Aufträgen

### Was ist stochastisches Prozess-Scheduling?

Bearbeitungszeiten sind nicht mehr bekannt wie beim deterministischen Prozess-Scheduling, sondern
eine stochastische Zufallsvariable mit bekannter Verteilung

### Warum ist die Bestimmung der Verteilung der Gesamtfertigungszeit nicht praxistauglich?

Selbst bei diskreter Verteilung der Bearbeitungszeit der Einzelprozesse ergeben sich schnell zu
viele mögliche Kombinationen, sodass der Aufwand schnell zu groß wird

### TODO

Jensensche Ungleichung (Erwartungswert Gesamtdauer ist höher als höher als höchster Erwartungswert
bei Paralleler Bearbeitung) Erwartungswert darf nicht statt Dichtefunktion verwendet werden Selbst
bei wenig Aufgaben ist Erwartungsfunktion nicht tauglich, weil damit der falsche kritische Pfad
identifiziert wird

### Welche Erweiterung der "Kritischer-Pfad-Methode" behandelt beschränkte Ressourcen?

Job-Shop-Probleme

### Was ist ein "Job-Shop-Problem"?

Ein Auftrag zerfällt in Teilaufträge, die gleiche Ressourcen benötigen. Aufträge deren Teilaufträge
gleiche Ressourcen benötigen, müssen in eine Reihenfolge gebracht werden.

### Was ist das "Job-Shop-Modell ohne Rezirkulation"?

ein Job-Shop-Problem bei dem jeder Auftrag jede Maschine höchstens einmal benötigt

### Wie werden Aufträge in einem Job-Shop-Modell ohne Rezirkulation notiert?

als Matrix mit Maschinennummern in Zeile 1 und Bearbeitungszeiten in Zeile 2, wobei jede Spalte
einen Teilauftrag darstellt

### Wann ist ein Zeitplan im Job-Shop-Modell zulässig?

- kein Teilauftrag wird vor seinem Vorgänger begonnen
- keine zwei Teilaufträge belegen dieselbe Maschine gleichzeitig

### Wie werden die Kanten im Präzedenzgraphen genannt, die die Bearbeitungsreihenfolge von Aufträgen festlegen?

Konjunktivkanten

### Was sind Diskunktivkanten?

Bidirektionale Kanten im Präzedenzgraphen, die zwischen Knoten liegen, die gleiche Ressourcen
benötigen

### Was ist eine "Disjunktivkantenbelegung"?

Im Präzedenzgraphen wird für jede Disjunktivkante eine Richtung ausgewählt. Die Auswahl der Richtung
aller Disjunktivkanten ist eine Disjunktivkantenbelegung.

### Wann ist eine Disjunktivkantenbelegung im Präzedenzgraphen zulässig?

wenn sie zyklenfrei ist

### Wie wird eine zulässige Disjunktivkantenbelegung konstruiert?

- Teilauftrag starten, dessen Vorgänger beendet ist und deren benötigte Maschine frei ist
- mehrere Kandidaten bei einer Maschine: zufällige Auswahl

### Wie wird eine optimale Disjunktivkantenbelegung gefunden?

Lösen eines diskreten Optimierungsproblems

### Wofür steht "divide and conquer" bei diskreten Optimierungsproblemen?

Bei "divide and conquer" wird versucht das Problem zu reduzieren und das Teilproblem zu optimieren.
Leider ist meist bei Betrachtung Gesamtproblems die optimale Lösung des Teilproblems nicht mehr
optimal.

### Was ist das "Shifting-Bottleneck-Verfahren"?

ein heuristisches Verfahren zum Finden einer guten Lösung eines Job-Shop Ablaufplans

### Wie funktioniert das "Shifting-Bottleneck-Verfahren" beim Job-Scheduling?

1. Ermitteln des Jobs mit der höchsten Gesamtbearbeitungszeit
2. Ermitteln der Maschine mit der höchsten Gesamtbelegungszeit (Bottleneck)
3. Höhere Bearbeitungszeit ist die untere Grenze der Bearbeitungszeit (Fälligkeitszeitpunkt)
4. Ermitteln der Fälligkeitszeiten der Teiljobs für Bottleneck Maschine: Von unterer Grenze so
   zurückrechnen, dass alle Folgeteilaufträge eines Jobs zur unteren Grenze erreicht werden können.
5. 1|$r_j$|$L_max$ - Verfahren für Bottleneck-Maschine
6. Im Baum mit der Reihenfolge mit der geringsten Überfälligkeit weitermachen

Mit der ermittelten Reihenfolge wird eine Disjunktivkantenbelegung für die Bottleneck Maschine
gemacht. Danach wird mit der Maschine mit der nächstkleineren Gesamtbelegungszeit weiter gemacht
(Shifting).

### Wie funktioniert "Branch-and-Bound" beim Job-Scheduling?

1|$r_j$|$L_max$ - Verfahren:
Es wird jeder Job einmal als erster Job festgelegt und die minimale Fertigungszeit unter der Annahme
unterbrechbarer / aufteilbarer Aufträge ermittelt (branch). Dies ist die untere Grenze für jede im
Baum darunterliegende Reihenfolge (bound). In der nächsten Ebene wird der zweite Job festgelegt und
wieder die untere Grenze ermittelt, wobei festgelegte Jobs nicht mehr als unterbrechbar / aufteilbar
behandelt werden. So wird der Baum in die Tiefe aufgebaut, wobei Äste wegen größerer Grenzen
vernachlässigt werden können.

### Wie können im Job-Shop-Modell Abhängigkeiten von Aufträgen untereinander modelliert werden?

zusätzliche Konjunktivkanten vom letzten Teilauftrag des Vorgängers zum ersten Teilauftrag des
abhängigen Auftrags

### Was ist das "Flow-Shop-Modell"?

ein spezielles Job-Shop-Modell, wo die Bearbeitungsreihenfolge aller Teilaufträge an den Maschinen
gleich ist
