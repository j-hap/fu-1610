---
recall: header
---

### Was ist makroskopische Verkehrsimulation?

die Simulation von Straßenverkehr durch Abbildung der kollektiven Gesamtdynamik

### Was zeichnet Makroskopische Verkehrsimulation aus?

Dynamik einzelner Verkehrsteilnehmer ist irrelevant, es wird die kollektive Gesamtdynamik abgebildet

### Was sind die interessanten Größen bei makroskopischer Verkehrsimulation?

- Verkehrsdichte $\rho$
- Geschwindigkeit $v$
- (Verkehrs-)Fluss $f$

### Was ist die Verkehrsdichte bei makroskopischer Verkehrssimulation?

Verkehrsdichte $\rho$ ist die Anzahl Fahrzeuge pro Kilometer Straße

### Was ist der Fluss bei makroskopischer Verkehrssimulation?

Fluss $f$ ist die Anzahl Fahrzeuge die pro Zeiteinheit einen Kontrollpunkt vorbeifahren

### Wie breiten sich Störungen im Verkehrsfluss aus?

wellenartig

### Was ist eine Störung im Verkehrsfluss?

alles, was einen Einfluss auf Dichte, Fluss oder Geschwindigkeit hat wie Ampel, Baustelle, Ende
eines Staus

### Womit kann die makroskopische Verkehrssimulation verglichen werden?

- Zähle Flüssigkeit in Kanalsystem
- kinematische Wellen in Flüssen

### Was ist das Lighthill-Whitham-Richards Modell?

ein einfaches Modell zur Simulation des Verkehrsflusses, das dynamische Charaktersitiken von Verkehr auf homogenen, unidirektionalen Fahrbahnen beschreiben kann

### Was ist die Grundlage des Lighthill-Whitham-Richards Modells?

Erhaltungssatz, hier Erhalt der Fahrzeuganzahl

### Was begrenzt die Verkehrsdichte nach oben?

die maximale Dichte ist erreicht wenn durchschnittlich lange Fahrzeuge Stoßstange and Stoßstange stehen

### Was zeichnet eine homogene Gleichgewichtsströmung in der Verkehrssimulation aus?

alle Fahrzeuge bewegen sich mit gleicher Geschwindigkeit und halten den gleichen Abstand ein, Geschwindigkeit, Verkehrsdichte und Fluss sind konstant

### Welchen Zusammenhang der drei Größen der makroskopischen Verkehrssimulation zeigen Messungen von Verkehrsströmung?

Geschwindigkeit und Fluss hängen von der Dichte ab.

### Was ist die Zustandsgleichung der makroskopischen Verkehrssimulation?

Fluss ist das Produkt von Dichte und Geschwindigkeit $f = \rho v$

### Was sind die drei Modellbedingungen in der makroskopischen Verkehrssimulation?

1. Ist die Straße frei, kann mit Maximalgeschwindigkeit gefahren werden: $\rho \rightarrow 0 \Rightarrow v \rightarrow v_{max}$
2. Ist die Straße voll, kommt der Verkehr zum erliegen: $\rho \rightarrow \rho_{max} \Rightarrow v \rightarrow 0$
3. Mit steigender Dichte fällt die Geschwindigkeit monoton

### Was ist die Stellschraube im Modell der makroskopischen Verkehrssimulation?

funktionaler Zusammenhang zwischen Dichte und Geschwindigkeit

### Was ist das Fundamentaldiagramm der makroskopischen Verkehrssimulation?

die Darstellung des funktionalen Zusammenhangs zwischen Fluss und Dichte, ergibt sich aus dem Einsetzen der Geschwindigkeits-Dichte-Beziehung in die Zustandsgleichung

### Was sagt das lokale Maximum im Fundamentaldiagramm der makroskopischen Verkehrssimulation aus?

Der maximale Fluss $f_{max}$ wird bei optimaler Dichte $\rho_{max}$ erreicht.

### Welche Bedeutung hat $\rho_{opt}$ für die Verkehrsplanung?

Ziel der Verkehrsplanung muss sein dieses $\rho_{opt}$ einzustellen um maximalen Fahrzeugdurchsatz zu erreichen.

### Warum wird in der Praxis für einen gegebenen Fluss $\neq f_{opt}$ meist die höhere der beiden möglichen Dichten erreicht?

Verkehrsteilnehmer fahren meist zu lange zu schnell

### Wie lässt sich ein makroskopisches Verkehrsmodell besser an die Realität anpassen?

Zusammenhang zwischen Dichte und Geschwindigkeit höherer Ordnung wählen und an gemessene Daten anpassen

### Was ist die Freiflussphase in der makroskopischen Verkehrssimulation?

der Bereich im Fundamentaldiagramm links von $f_{max}$

### Was ist die Stauphase in der makroskopischen Verkehrssimulation?

der Bereich im Fundamentaldiagramm rechts von $f_{max}$

### Wie lautet die Kontinuitätsgleichung der makroskopischen Verkehrssimulation?

$$
\frac{\partial}{\partial t} \rho(x,t) + \frac{\partial}{\partial x} f(x,t) = 0
$$

### Wie lautet die quasistationäre Kontinuitätsgleichung der makroskopischen Verkehrssimulation?

$$
\frac{\partial}{\partial t} \rho(x,t) + \frac{\partial}{\partial x} f(\rho(x,t)) = 0
$$

### Wie wird die quasistationäre Kontinuitätsgleichung der makroskopischen Verkehrssimulation noch genannt?

Verkehrsgleichung

### Was ist ein Prädiktor-Korrektor-Verfahren?

Mehrschrittverfahren in dem mit einem expliziten Einschrittverfahren 

### Welchen Vorteil hat ein Prädiktor-Korrektor-Verfahren gegenüber einem Einschrittverfahren?

numerische Stabilität

### Was ist die "Signalgeschwindigkeit" der makroskopischen Verkehrssimulation?

Ableitung des Flusses nach der Dichte, gibt an mit welcher Geschwindigkeit sich eine Störung im Verkehr ausbreitet

### Was ist die "Verkehrsgeschwindigkeit" der makroskopischen Verkehrssimulation?

die Geschwindigkeit der Fahrzeuge, explizite Nennung, um sie von der Signalgeschwindigkeit abzusetzen

### Welches Verhältnis besteht zwischen Signalgeschwindigkeit und Verkehrsgeschwindigkeit?

Die Signalgeschwindigkeit ist stets $\leq$ Verkehrsgeschwindigkeit

### Was passiert mit der Signalgeschwindigkeit bei optimaler Verkehrsdichte?

sie wird zu Null, der Stau bleibt also an Ort und Stelle und wird nicht abgebaut

### Wie nennt man Oszillationen vor und nach einem Dichtesprung in der makroskopischen Verkehrssimulation?

Wiggles, hervorgerufen durch Überreaktion, das zu kurzfristigem Stop-and-Go führt

### Wie werden Kurven konstanter Signalgeschwindigkeit genannt?

Charakteristiken
