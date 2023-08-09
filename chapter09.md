---
recall: header
---

### Wozu dient die stochastische Verkehrssimulation?

Simulation von Auftragsverkehr durch ein System, um Schwachstellen und Flaschenhälse zu
identifizieren, die das Gesamtsystem ausbremsen oder Überkapazität des Systems einsparen zu können

### Was zeichnet die stochastische Verkehrssimulation im Gegensatz zur mikroskopischen und makroskopischen aus?

stochastische ist wie makroskopische an Durchschnittswerten interessiert von 
- Durchlaufzeiten
- Wartezeiten

betrachtet aber wie die mikroskopische einzelne Objekte / Aufträge / Teilnehmer des Systems. Hierbei
ist allerdings nur das Verhalten der Teilnehmer an bestimmten Punkten interessant, nicht der gesamte
Verlauf von Start bis Ziel

### Was ist ein "Warte- und Bediensystem"?

ein System aus ggf. mehreren Warteschlangen in die sich Aufträge einreihen und darauf warten an ggf.
mehreren Bedieneinheiten bearbeitet zu werden

### Wie können Eingabeparameter einer stochastischen Verkehrssimulation ermittelt werden?

empirische Messungen realer Systeme, zum Beispiel Fahrzeugzählungen, Kundenzählungen etc.

### Was ist der "Rebound-Effekt" (aus den "Feedback-Effekten")?

Funktioniert ein System gut, lockt es mehr Aufträge / Kunden an, was zu höherer Auslastung führt und
damit zu schlechterer Funktion (schnellste Spur im Stau, schnellste Kasse, ...)

### Was ist ein elementares Wartesystem?

Kombination aus Warteschlange (WS) und Bedieneinheit (ggf. mehrere) (BE)

### Wie wird ein elementares Wartesystem noch genannt?

Bedienstation

### Was ist die Kapazität $m$ einer elementaren Warteschlange / Bedienstation?

die Anzahl der Bedieneinheiten

### Welchen Parameter besitzt eine Warteschlange?

Kapazität $k$

### Was ist die "Zwischenankunftszeit"?

die Zeit, die zwischen der Ankunft von zwei Aufträgen in einem Wartesystem vergeht

### Was ist die Ankunftsrate $\lambda$?

die mittlere Anzahl von Aufträgen, die pro Zeiteinheit eintreffen

### Wie wird die Ankunftsrate $\lambda$ berechnet?

Kehrwert der mittleren Zwischenankunftszeit

### Was ist ein stationärer stochastischer Prozess?

eine Folge gleichartiger, zeitlich geordneter Vorgänge, deren Verteiltung im betrachteten Zeitraum
nur von der Intervalllänge abhängt

### Wie hängen Exponentialverteilung und Poisson-Prozess zusammen?

Ein Poisson-Prozess zählt Ereignisse mit exponentialverteilter Zwischenankunftszeit. Die
"Intensität" des Poisson-Prozess ist die Anzahl Sprünge (Ereignisse), die pro Zeiteinheit zu
erwarten sind. Das entspricht genau dem Parameter der negativen Exponentialverteilung.

### Wie lautet die Dichtefunktion der Exponentialverteilung?

$$ f(t) = \lambda e ^ {-\lambda t} $$

### Wie lautet die Verteilungsfunktion der Exponentialverteilung?

$$ F(t) = 1 - e ^ {-\lambda t} $$

### Was bedeutet es, dass die Exponentialverteilung gedächtnislos ist?

im Falle eines Ausfalls: Die Wahrscheinlichkeit, dass ein Bauteil noch x Jahre überlebt, wenn es
schon y Jahre überlebt hat, ist genauso groß, wie dass ein neues Bauteil x Jahre überlebt  

im Falle der Ankunft eines Kunden: Die Wahrscheinlichkeit, dass in den nächste x Minuten ein neuer
Kunde ankommt, wenn seit y Minuten keiner gekommen ist, ist genauso groß, wie dass ein Kunde in den
ersten x Minuten nach Öffnung ankommt

### Was ist das Wartezeitparadox?

Wartet man auf ein exponentialverteiltes Ereignis ist die erwartete Wartezeit ebenso lang wie der
Erwartungswert der Zwischenankunftszeit

### Welche einheitliche Beschreibung von Wartesystemen hat sich durchgesetzt?

Kendall-Notation

### Was ist die "Kendall-Notation" und wie ist sie aufgebaut?

einheitliche Beschreibung von Wartesystemen Aufbau:

A/B/m/k/n/D

mit
- A: Verteilung der Ankünfte
- B: Verteilung der Bedienzeiten
- m: Anzahl unabhängiger Bedieneinheiten
- k: Kapazität der Warteschlange (default: $\infty$)
- n: Anzahl aller möglichen Aufträge (bei geschlossenen Systemen interessant, sonst $\infty$)
- D: Warteschlangendisziplin / Bedienstrategie (default: FCFS)

### Welche Verteilungen werden wie in der Kendall-Notation notiert?

- D: Deterministische Verteilung (konstante Zeitintervalle)
- M: Exponentialverteilt (memoryless)
- G: Allgemeine, beliebige (general) Verteilung

### In welche zwei Kategorien werden Bedienstrategien unterschieden?

verdrängende / nicht verdrängende

### Welche nicht-verdrängenden Bedienstrategien gibt es?

- Zufällige Auswahl des nächsten Auftrags (Cocktailbar)
- First-Come-First-Served (Supermarkt)
- Last-Come-First-Served (Auftragsstapel (buchstäblich))
- Prioritätsbasiert (Krankenhaus)

### Welche verdrängenden Bedienstrategien gibt es?

- Round-Robin: Feste Zeitspanne pro Auftrag und Rotation
- LCFS-preemptive: Neue Aufträge werden sofort begonnnen (bevor aktuelle abgeschlossen sind)
- Prioritätsbasiert
  - statisch: neue Aufträge mit hoher Priorität verdrängen niedrigere
  - dynamisch: Priorität kann sich über Zeit ändern

### Welcher Overhead entsteht bei verdrängenden Bedienstrategien?

Anhalten und Sichern des aktuellen Bearbeitungsstand des unterbrochenen Systems

### Was sind die sieben Leistungsgrößen eines Wartesystems?

- Verweilzeit $y$
- Wartezeit $w$
- Bedienzeit $b$
- Füllung $f$
- Durchsatz $d$
- Grenzdurchsatz $c$
- Auslastung $\rho$

### Wie ergibt sich die Verweilzeit $y$ eines Wartesystems?

Summe aus Warte- und Bedienzeit

### Wie ergibt sich die Wartezeit $w$ eines Wartesystems?

Zeit zwischen Ankunft in der Warteschlange und Beginn der Bedienung an einer Bedieneinheit

### Wie ergibt sich die Bedienzeit $b$ eines Wartesystems?

Zeit zwischen Beginn der Bedienung an einer Bedieneinheit und Abschluss der Bedienung

### Was ist die Füllung $f$ eines Wartesystems?

Anzahl der Aufträge im Wartesystem

### Wie ergibt sich der Durchsatz $d$ eines Wartesystems?

mittlere Anzahl der in einem Zeitintervall vollendeten Aufträge

### Was ist der Grenzdurchsatz $c$ eines Wartesystems?

maximal möglicher Durchsatz

### Wie ergibt sich die Auslastung $\rho$ eines Wartesystems?

Durchsatz geteilt durch den Grenzdurchsatz

### Was ist die Formel von Little?

zentraler Satz der Verkehrstheorie, der einen Zusammenhang zwischen mittlerer Füllung, mittlerem
Durchsatz und mittlerer Verweilzeit herstellt

$$ \overline{f}(t_1, t_2) = d(t_1, t_2) \cdot \overline{y}(t_1, t_2) $$

bzw. der Erwartungswerte für stochastische Größen (Zufallsvariablen)

$$ E(F) = E(D) \cdot E(Y) $$

### Wie hängen die Formel von Little und die Zustandsgleichung der makroskopischen Verkehrssimulation zusammen?

- Füllung $\widehat{=}$ Verkehrsdichte
- Durchsatz $\widehat{=}$ Verkehrsfluss
- Verweilzeit $\widehat{=}$ Geschwindigkeit$^{-1}$

### Wie berechnet sich der Grenzdurchsatz einer Bedieneinheit?

$$ c_{BE} = \frac{m}{E(B)} $$

Wobei $m = 1$ bei einer einzelnen Bedieneinheit

### Was ist ein Warteschlangennetz?

ein System aus mehreren elementaren Bedienstationen unterschiedlicher Charakteristika

### In welche zwei Kategorien werden Warteschlangennetze unterschieden?

offen / geschlossen

### Was unterscheidet offene von geschlossenen Warteschlangensystemen?

In geschlossenen Netzen ist die Anzahl der Aufträge, die darin zirkulieren konstant (konstante
Füllung). In offenen Netzen kommen Auträge ins Netz und verlassen es auch wieder (variable Füllung)

### Was geschieht mit bearbeiteten Aufträgen in einem geschlossenen Warteschlangennetz?

stellen sich vorn im System wieder an

### Welche Parallelen können zwischen Warteschlangennetzen und Job-Shop-Problemen gefunden werden?

Ein Auftrag, der mehrere Bedienstationen in einem Warteschlangennetz besucht, kann wie ein Auftrag
mit mehreren Teilaufträgen bestimmter Reihenfolge im Job-Shop-Problem betrachtet werden.

### Wie werden die stochastisch auftretenden Bedienreihenfolgen in Warteschlangennetzen modelliert?

Transitionswahrscheinlichkeiten an den Kanten des Netzes entscheiden über den Weg eines Auftrags
durchs Netz

### Was ist die "Besuchszahl" in einem Warteschlangennetz?

Die Besuchszahl $v_i$ beschreibt wie oft ein Auftrag an der Bedienstation $i$ bearbeitet wird

### Wie kann es dazu kommen, dass der Durchsatz an einer elementaren Bedienstation größer ist als die im Warteschlangennetz?

Muss ein Auftrag beim Durchlauf durch das Warteschlangennetz mehrfach dieselbe elementare
Bedienstation passieren, muss deren Durchsatz höher sein als der des Gesamtnetzes

### Was ist ein "Verkehrsengpass" in einem Warteschlangennetz?

die elementare Bedieneinheit, die bei Erhöhung des Durchsatzes des Systems zuerst den
Grenzdurchsatz, also eine Auslastung von 1, erreicht

### Wie ergibt sich die erwartete Bedienzeit in einem Warteschlangennetzes?

$$ E(B_s) = \sum _i v_i E(B_i) $$

### Wie ergibt sich der Grenzdurchsatz eines Warteschlangennetzes?

Der Grenzdurchsatz hängt vom Grenzdurchsatz des Verkehrsengpass ab und wird durch die nötige Anzahl
der besuche reduziert

$$ c_S = \frac{c_{VE}}{v_{VE}} $$

### Wie ergibt sich die Sättigungsfüllung eines Warteschlangennetzes?

$$ f^*_S = c_S \cdot E(B_S) $$

### Was ist ein stationären Grenzprozess?

Ist der Erwartungswert einer Zustandsgröße (zum Beispiel Füllung) eines Prozesses nur nach langer
Zeit konstant, ist es ein stationärer Grenzprozess.

### Wie nennt man den Zeitraum eines stationären Grenzprozess bis die stationäre Phase erreicht ist?

Einschwingphase / transiente Phase

### Wie können stochastische Prozesse klassifiziert werden?

diskrete / kontinuierliche Zeit / Zustandsmenge:
- zeitdiskreter, wertdiskreter Prozess
- zeitdiskreter, reelwertiger Prozess
- zeitstetiger, wertdiskreter Prozess
- zeitstetiger, reelwertiger Prozess

### Was zeichnet einen kontinuierlichen Prozess aus?

Der Zustandsraum ist nicht abzählbar, also die Menge der rationalen Zahlen.

### Was zeichnet einen diskreten Prozess aus?

Der Zustandsraum ist endlich oder abzählbar.

### Wie wird der Prozess der Zwischenankunftszeiten klassifiziert?

zeitdiskreter, reelwertiger Prozess: $i$-te Ankunft ($i \in \mathbb{N}$) zur Zeit $t$ ($t \in
\mathbb{R}$)

### Wie wird der Prozess des Zählen von exponentialverteilten Ereignissen (Poisson-Prozess) klassifiziert?

zeitstetiger, wertdiskreter Prozess: nach ($t \in \mathbb{R}$) sind $n$ ($n \in \mathbb{N}$)
Ereignisse passiert

### Was ist der Unterschied zwischen Markov-Prozess und Markov-Kette?

häufig synonym verwendet, aber manchmal bezeichnet die Markov-Kette nur Prozesse mit diskretem
Zustandsraum und der Markov-Prozess Prozesse mit kontinuierlichem Zustandsraum

### Was ist die Markov-Eigenschaft?

Der Folgezustand eines Prozesses hängt nur vom aktuellen Zustand und nicht von der Historie ab. Im
aktuellen Zustand ist alles enthalten, was wir über die Vergangenheit wissen

### Was ist ein homogener Markov-Prozess?

In einem homogenen Markov-Prozess sind die Übergangswahrscheinlichkeiten der Zustände konstant und
damit unabhängig von der Zeit

### Was ist ein homogener Geburts-Todes-Prozess?

ein homogener Markov-Prozess (genauer Markov-Kette), in dem sich der Zustand beim Zustandsübergang
nur um 1 verändert

### Wofür steht die Abkürzung HBDP?

homogeneous birth-death process

### Was ist ein Random Walk?

stochastischer Prozess bei dem Zuwächse / Abnahmen des aktuellen Zustands gleichverteilt zufällig
passieren

### Was sagt die "Chapman-Kolmogorow-Gleichung" aus?

dass die Wahrscheinlichkeit für das Erreichen eines Zustands in einer Markov-Kette über die
Wahrscheinlichkeiten von Zwischenzuständen ausgedrückt werden kann

### Was ist eine irreduzible Markov-Kette?

eine Markov-Kette bei der alle Zustände aus jedem anderen Zustand erreichbar sind (ggf. über
Zwischenzustände)

### Was ist eine rekurrente Markov-Kette?

eine Markov-Kette bei der man mit Sicherheit von einem Zustand aus irgendwann wieder in diesem
Zustand landet

### Was ist die "Rekurrenzzeit"?

Erwartungswert der Zeit, die es braucht, um in einem rekurrenten Markov-Prozess wieder in in einen
Zustand zurückzukehren

### Wann ist ein Zustand in einem Markov-Prozess positiv rekurrent?

wenn die Rekurrenzzeit endlich ist

### Wann ist ein Zustand in einem Markov-Prozess nullrekurrent?

wenn die Rekurrenzzeit unendlich ist

### Wann ist ein Zustand in einem Markov-Prozess transient?

wenn die Rückkehrwahrscheinlichkeit $<1$ ist

### Wann ist ein Zustand in einem Markov-Prozess periodisch?

wenn man nur mit einem ganzzahligen Vielfachen einer Periodenlänge in den Zustand zurückkehrt

### Was gilt für die Rekurrenzeigenschaften der Zustände in einer irreduziblen homogenen Markov-Kette?

alle Zustände sind entweder
- transient
- positiv rekurrent oder 
- nullrekurrent

### Was gilt für die Zustände einer irreduziblen homogenen Markov-Kette wenn ein Zustand periodisch ist?

alle sind periodisch

### Warum ist der reine Geburtsprozess nicht irreduzibel?

der Prozess kann nicht zurück in Zustände geringerer Population als der aktuellen gelangen

### Warum ist der reine Geburtsprozess nicht stationär?

die Übergangswahrscheinlichkeit zur nächstgrößeren Population hängt von der Populationsgröße ab, die
mit der Zeit wächst, also steigt auch die Übergangswahrscheinlichkeit mit der Zeit

### Was ist die stationäre Grenzverteilung einer Markov-Kette?

Die stationäre Grenzverteilung gibt an mit welcher Wahrscheinlichkeit ein Zustand in einer
Markov-Kette nach unendlicher Zeit angenommen wird, unabhängig vom Startzustand

### Was ist die Vorraussetzung für die Existenz eines stationären Grenzprozess?

alle Zustände sind positiv rekurrent

### Was ist die Transitionsmatrix einer Markov-Kette?

für $k$ mögliche Zustände enthält die $k \times k$ große Transitionsmatrix $P$ die
Wahrscheinlichkeiten aller Zustandsübergänge

### Wie kann der stationäre Grenzzustand eines Markov-Prozesses berechnet werden?

Der Grenzzustand ist Fixpunkt der Zustandsübergangsgleichung $$ P^T \pi = \pi $$ wobei $P$ die
Transitionsmatrix und $\pi$ die Verteilung der Vektor der Zustandswahrscheinlichkeiten ist. Lösen
des Gleichungssystems liefert den Grenzzustand, unabhängig vom Startzustand

### Wann ist ein Wartesystem stabil?

wenn die Warteschlange niemals unendlich lang werden kann, das ist entweder der Fall wenn
- die Warteschlange endliche Kapazität hat
- die Population (der Aufträge) endlich ist oder
- die Ankunftsrate kleiner als die Bedienrate aller Bedieneinheiten ist $$ \lambda < m \mu $$

### Wie werden Wartesysteme mit endlich langer Warteschlange genannt?

Verlustsystem, weil Aufträge abgewiesen werden wenn die Warteschlange voll ist

### Wie berechnet sich der Erwartungswert der Füllung eines $M/M/1$ Wartesystems?

$$ E(F) = \frac{\lambda}{\mu - \lambda} $$

### Wie berechnet sich die Auslatung eines $M/M/1$ Wartesystems im statioären Grenzzustand?

$$ \rho = \frac{\lambda}{\mu} $$

### Wie berechnet sich der Erwartungswert der Füllung eines $M/M/\infty$ Wartesystems?

$$ E(F) = \frac{\lambda}{\mu} $$

### Wie berechnet sich die Auslatung eines $M/M/m$ Wartesystems im statioären Grenzzustand?

$$ \rho = \frac{\lambda}{m\mu} $$

### Was ist eine diskrete Ereignissimulation?

eine Simulation, die nur zu Zeitpunkten simuliert wird, bei denen ein Ereignis stattfindet

### Wofür steht die Abkürzung DES?

diskrete event simulation (diskrete Ereignissimulation)

### Welche Datenstrukturen eigenen sich zur Modellierung der Warteschlange von Ereignissen bei der diskreten Ereignissimulation?

Datenstruktur, die automatisch Ordnung herstellt und die Entnahme des Ereginisses mit dem nächsten
Zeitstempel ermöglicht, zum Beispiel Fibbibonacci-Heap 

### Wie wird Straßenverkehr auf Basis der stochastischen Verkehrssimulation modelliert?

- Verkehrsteilnehmer sind Aufträge des Systems
- Straßen sind Wartesysteme endlicher Kapazität
- Bedienzeit (Fahrtzeit) hängt von Füllung (Verkehrsdichte) ab
- Kreuzungen sind Bedienstrationen

### Welchen Vorteil hat die Modellierung des Straßenverkehrs als stochastischen Verkehrssimulation?

Weniger Rechenaufwand als mikroskopische Simulation, weil nur noch die Bedienzeit pro Straßen /
Kreuzung bestimmt werden muss, statt das Vorankommen einzelner Verkehrsteilnehmer

