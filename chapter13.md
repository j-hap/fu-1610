---
recall: header
---

### Womit beschäftigt sich die Molekulardynamik?

Simulation von Stoffen auf molekularer bzw. atomarer Ebene

### Wo kommt die Simulation von Molekulardynamik zum Einsatz?

- biologische oder medizinische Anwendungen:
  - Funktion von Proteinen
  - Funktion von Makromolekülen
  - Nanotechnik
- Materialwissenschaften
- Verfahrenstechnik
- Simulation von Stoffgrenzen

### Was ist die wesentliche Herausforderung der Molekulardynamik?

Berechnung der auf jedes Molekül einwirkenden Kräfte (u.A. aus Wechselwirkungen mit anderen
Molekülen)

### Was ist das "Hard-Sphere-Model"?

eine Modellvereinfachung, bei der Atome als harte Kugeln modelliert werden, die sich bei
Zusammenstößen ebenso verhalten

### Was sind die vier fundamentalen Kräfte?

- Gravitation
- Elektromagnetische Kraft
- starke Kernkraft
- schwache Kernkraft

### Welche Rolle spielt die Gravitation zwischen Molekülen in der Simulation von Molekulardynamik?

keine, sie ist so gering, dass sie vernachlässigt werden kann

### Welche Rolle spielt die elektromagnetische Kraft zwischen Molekülen in der Simulation von Molekulardynamik?

sie ist hauptverantwortlich für Kräfte zwischen Atomen und spielt damit die größte Rolle

### Welche Rolle spielt die starke Kernkraft zwischen Molekülen in der Simulation von Molekulardynamik?

keine, sie wirkt nur auf so kurzen Distanzen und damit nur im Atomkern, was aber in der Simulation nicht interessant ist

### Welche Rolle spielt die schwache Kernkraft zwischen Molekülen in der Simulation von Molekulardynamik?

keine, sie wirkt nur auf so kurzen Distanzen und damit nur im Atomkern, was aber in der Simulation nicht interessant ist

### Was ist die Definition eines "Potentials" in der Partikel-Simulation?

Vermögen eine Kraft auf einen anderen Partikel auszuüben

### Was ist ein "Paar-Potential"?

ein Potential zwischen zwei Partikeln, das vom Abstand der Partikel abhängt

### Wie berechnet sich die Kraft aus einem Potential?

der Kraftvektor $F$ entspricht dem negativen Gradienten des Potentials $U$

### Was ist die "van-der-Waals-Kraft"? 

eine anziehende Kraft zwischen Atomen, die sich nahe kommen, die auf die elektromagnetische Kraft zurückgeht

### Wie entsteht die van-der-Waals-Kraft?

Atome bilden durch inhomogene verteilung der Elektronen temporäre Bipole, die Atome in der Nähe
ebenfalls zu Bipolen machen, indem dessen Elektronen vom negativen Pol des ersten abgestoßen werden.
Dadurch entsteht eine Anziehung zwischen Atomkern des einen und negativem Pol
("Elektronenansammlung") des anderen Atoms

### Was ist die "Pauli-Repulsion"?

eine abstoßende Kraft zwischen Atomen, die sich nahe kommen, die auf die elektromagnetische Kraft zurückgeht

### Wie entsteht die Pauli-Repulsion?

kommen sich Atome so nah, dass die Elektronenwolken überlappen, stoßen diese sich gegenseitig ab

### Was ist das "Lennard-Jones-Potential"?

die Kombination aus van-der-Waals-Kraft und Pauli-Repulsion

### Was sind "Lennard-Jones-Zentren"?

ein Ersatzmodell für Atome zur Verwendung mit dem Lennard-Jones-Potential, das über Energie
$\varepsilon$ und Größe $\sigma$ parametiert werden

### Wozu werden Mischregeln bei der Berechnung von Kräften zwischen Partikeln verwendet?

unterscheiden sich die Partikel in den Parametern, die für die Berechnung der Kraft notwendig sind, muss aus den Parameterpaaren ein gemittelter Wert nach bestimmten Mischregeln berechnet werden

### Was ist der Abschneideradius?

eine Distanz zwischen Partikeln oberhalb der die Wechselwirkungen zwischen ihnen vernachlässigt
wird

### Welchen Vorteil bietet die Verwendung des Abschnederadius bei der Berechnung von Parikelkäften?

Es müssen nicht alle Partikel im Simulationsraum berücksichtigt werden. Bei Gleichverteilung der Partikel im Raum ist die Anzahl der Partikel innerhalb des Abschneideradius konstant, womit sich der Aufwand für die Kraftberechnung aller Partikel von $\mathcal{O}(n^2)$ auf $\mathcal{O}(n)$ verringert

### Was ist das "Velocity-Störmer-Verlet-Verfahren"?

ein Verfahren zweiter Ordnung zum numerischen Lösen von Differentialgleichungen

### Wie ist der Ablauf des "Velocity-Störmer-Verlet-Verfahren"?

1. Berechnung der neuen Position aus bekannter aktueller Position, Geschwindigkeit und Beschleunigung
2. Berechnung der neuen Kraft auf die Partikel auf Basis der neuen Position
3. Berechnung der neuen Beschleunigung auf Basis der Kraft
4. Berechnung der neuen Geschwindigkeit durch Kombination eines "halben" expliziten und eines halben implitizen Euler-Schritts und der alten und neuen Beschleunigung

### Wie wird der Speicherbedarf des Velocity-Störmer-Verlet-Verfahrens reduziert?

1. Berechnung der neuen Position aus bekannter aktueller Position, Geschwindigkeit und Beschleunigung
2. Berechnung der Zwischengeschwindigkeit durch einen halben expliziten Euler-Schritt
3. Berechnung der neuen Kraft auf die Partikel auf Basis der neuen Position
4. Berechnung der neuen Beschleunigung auf Basis der Kraft
5. Berechnung der neuen Geschwindigkeit durch einen halben impliziten Euler-Schritt
  
Dadurch müssen nicht zwei Beschleunigungen pro Partikel gespeichert werden

### Welche Vorteile bietet das Velocity-Störmer-Verlet-Verfahren gegenüber dem Euler-Verfahren?

geringerer Fehler als Euler (bei kleinen Schrittweiten), weil der lokale Fehler bei einem Verfahren zweiter Ordnung in $\mathcal{O}(\Delta t^3)$ und damit der gesamte Diskretisierungsfehler in $\mathcal{O}(\Delta t^2)$ liegt

### Was ist das Ziel der Simulation von Moleküldynamik?

Aussagen über makroskopische Größen des Simulationsgebiets wie Temperatur, Druck und potentielle Energie

### Was ist ein NVT-Ensemble?

ein Tripel aus konstanten (!) Bedingungen für ein Simulationsgebiet bei der Simulation von
Moleküldynamik
- N: Anzahl Partikel
- V: Volumen des Simulationsgebiets
- T: Temperatur des Stoffes

### Wie hängen die kinetische Energie von Partikeln und die Temperatur im Simulationsgebiet zusammen?

über die Boltzmann-Konstante lässt sich aus der Summe der kinetischen Energie aller Partikel die Temperatur im Simulationsgebiet bestimmen

### Wie kann bei einer Simulation von Moleküldynamik die Temperatur konstant gehalten werden?

Skalierung der Partikelgeschwindigkeiten, um die kinetische Energie konstant zu halten

### Was sind reflektierenden Randbedingungen?

in der Partikelsimulation können Partikel das Simulationsgebiet nicht verlassen, sondern prallen am Rand der Simulationsgebiets ab

### Was sind periodische Randbedingungen in der Partikelsimulation?

Partikel, die das Simulationsgebiet an einem Rand verlassen, betreten das Gebiet auf der anderen Seite mit gleicher Geschwindigkeit und Beschleunigung

### Welche Randbedingungen eigenen sich, um die Partikelanzahl im Simulationsgebiet konstant zu halten?

- reflektierende
- periodische

### Welchen Vorteil haben periodische Randbedingungen gegenüber reflektierenden?

Das Simulationsgebiet ist für gewöhnlich ein Ausschnitt aus einer größeren Welt ohne harte Grenzen,
sodass auch Interaktionen außerhalb des Simulationsgebiets stattfinden. Periodische Randbedingungen
bieten bessere Vorraussetzungen das abzubilden.

### Welches Problem besteht bei periodischen Randbedigungen in Verbindung mit einem Abschneideradius, der größer als das Simulationsgebiet ist?

Partikel können sich selbst beeinflussen, weil ihre virtuellen Kopien genau die Größe des Simulationsgebiets von ihnen entfernt liegen

### Wie wird mittels Abschneideradius und linked-cells-Algorithmus der Rechenaufwand für die Wechselwirkungen der Partikel reduziert?

- in $\mathcal{O}(n)$ kann jeder Partikel in eine Zelle eingeordnet werden
- für jeden Partikel müssen nur Partikel der eigenen Zellen und der benachbarten Zellen mit größerem Index bestimmt werden
- wegen der Symmetrie der Wechselwirkung, ergibt sich die Wechselwirkung mit Partikeln in Zellen mit kleinerem Index automatisch aus vorheriger Berechnung

### Wie kann Partikelsimulation parallelisiert werden?

Simulationsgebiet wird in Teilgebiete unterteilt, Nachbarn der Randzellen müssen beim benachbarten Prozess / Thread abgefragt werden
