---
recall: header
---

### Was ist Simulation?

- allgemein: Vorausberechnung oder Nachstellung eines realen Szenarios im Computer
- speziell: Berechnungsprozess eines Simulationsmodells

### Was sind "virtuelle Experimente"?

anderer Name für "Simulation"

### Was sind die Vorteile "virtueller Experimente"?

echte Experimente
- wegen zugrundeliegender Zeit- und Raumskalen unmöglich (Astrophysik)
- unerwünscht (Kernwaffen, Tierversuche, ...)
- fordern zu großen Aufwand (Teilchenbeschleuniger)

### Wie steht die Simulation zu theoretischer und experimenteller Analyse eines Problems?

ergänzt, ersetzt nicht

### Was sind die Ziele von Simulation?

- Nachvollziehen bekannter Szenarien um sie besser zu verstehen (Katastrophen, Unfälle, ...)
- Vorhersage unbekannter Szenarien (Klima, Wetter, Weltbevölkerung, ...)
- Optimierung von Szenarien (Einsatzpläne, Wirkungsgrade, ...)

### Was ist die Simulationspipeline?

Ablauf einer Simulation mit mehreren Teilschritten und möglichen Iterationsschleifen

### Aus welchen 6 Schritten besteht die Simulationspipeline?

- Modellierung
- Berechnung
- Implementierung
- Visualisierung
- Validierung
- Einbettung

### Was passiert im Schritt "Modellierung" der Simulationspipeline?

Erstellen eines vereinfachten, geeigneten Abbilds / Ausschnitts des Betrachtungsgegenstands (Beispiele: Mehrkörpersimulation, FEM, DEM, ...)

### Was passiert im Schritt "Berechnung" der Simulationspipeline?

Aufbereiten des Modells, um es berechnen zu können (Diskretisierung, Solver auswählen, Algorithmen entwickeln)

### Was passiert im Schritt "Implementierung" der Simulationspipeline?

Entwickelte Algorithmen werden möglichst effizient in Software umgesetzt

### Was passiert im Schritt "Visualisierung" der Simulationspipeline?

Darstellung der Berechnungsergebnisse in interpretierbarer Form

### Was passiert im Schritt "Validierung" der Simulationspipeline?

Abgleich der Ergebnisse mit anderen Modellen / anderen Algorithmen / anderen Implementierungen um
Verlässlichkeit der eigenen Simulation zu gewährleisten. Auch Abgleich mit Experiementen sinnvoll

### Was passiert im Schritt "Einbettung" der Simulationspipeline?

Die Simulation im Gesamtkontext einsetzbar machen. Dazu werden Schnittstellen definiert und umgesetzt. Beispiel: Automatische Neuberechnung der Festigkeit eines Bauteils bei geänderter Konstruktion

### Was ist ein Modell?

- (vereinfachtes) Abbild einer (partiellen) Realität
- formale, mathematische Beschreibungen

### Was ist die mathematische Modellierung / Modellbildung?

Prozess der formalen Herleitung und Analyse eines mathematischen Modells für einen Effekt, ein
Phänomen oder ein technisches System

### Wie läuft typischerweise die mathematische Modellierung / Modellbildung ab?

nichtformale Beschreibung des betreffenden Modellierungsgegenstands -> semiformale Beschreibung (mittels Instrumentarium der Anwendungsdisziplin) -> streng formale (widerspruchsfreie, kon-
sistente) Beschreibung (mathematisches Modell)

### Was sind Disziplinen in denen heute mathematische Modelle verwendet werden?

- Astrophysik (Entstehung und Entwicklung des Universums)
- Geophysik (Entstehung von Erdbeben)
- Plasmapysik (Fusion)
- Proteinforschung (räumliche Struktur und Wirkung)
- theoretische Chemie (Ursachen von Materialverhalten auf atomarer Ebene)
- Drug Design (Entwurf von Wirkstoffen)
- Medizin (Untersuchung von Aneurismen, Optimierung von Implantaten)
- Klimaforschung (Ozeanströme, Ozonloch)
- Wettervorhersage
- Automobilindustrie (Crashtest - Strukturmechanik, Tiefziehen - Strukturoptimierung, Aerodynamik / Klimatisierung - Strömungsmechanik, Schallabstrahlung - Aeroakustik, Einspritzung - Verbrennung, Fahrdynamik - Optimalsteuerung, Sensorik & Aktorik - Mechatronische Systeme)
- Halbleiterindustrie (Bauelementsimulation, Prozesssimulation, Schaltkreissimulation)
- Nationalökonomie (Konjunkturverlauf, Wirtschafts- und Fiskalpolitik, Preisbildung) (keine Konsensmodelle)
- Banken und Versicherungen (Bewertung von Finanzderivaten)
- Verkehrstechnik (Staubildung, Routenplanung)
- Versorger (Netzauslastung)
- Logistik (Fuhrparkmanagement)
- Stadtplanung, Epidemiologie (Populationsmodelle)
- Meinungsforschung
- Computerspiele (Beleuchtungsmodelle)

### Was sind die drei zentralen Fragen der Modellierung?

1. Wie kommt man zu einem geeigneten Modell?
2. Welche Beschreibungsmittel nimmt man dafür her?
3. Wie bewertet man dann anschließend die Qualität des hergeleiteten Modells?

### Wie läuft die Modellierung ab?

- Festlegen 
  - des räumlichen und zeitlichen Rahmens der Simulation
  - der nötigen Genauigkeit (Auflösung) der Ergebnisse
- Bewerten der Einflussgrößen (qualitativ) und das Maß des Einflusses (quantitativ)
- Festlegen des Simulationsziels (Vorhandensein einer Lösung, irgendeine Lösung, einzige Lösung, optimale Lösung)

### Was ist das mathematische Instrumentarium für die Modellbildung?

- algebraische Gleichungen / Ungleichungen
- Systeme gewöhnlicher Differentialgleichungen (nur eine Unabhängige)
- Systeme partieller Differentialgleichungen (mehrere Unabhängige)
- Automaten / Zustandsdiagramme
- Graphen
- Wahrscheinlichkeitsverteilungen
- regelbasierte Systeme / Fuzzy Logic
- neuronale Netze
- Sprachkonzepte (z.B. UML)
- algebraische Strukturen (Gruppen, Ringe, endliche Körper)

### Worum geht es bei der Analyse von Modellen?

Bewertung der Handhabbarkeit und Zweckmäßigkeit

### Was bedeutet die "Lösbarkeit" eines Modells?

Ein Modell ist lösbar, wenn es unter der gegebenen Fragestellung eine Antwort liefert. Hierbei ist interessant, ob das Modell keine, eine oder mehrere Lösungen hat. Beispiele:
- stationäre Grenzzustände von Populationsmodellen
- Zyklenfreiheit des Präzedenzgraphen bei schrittweiser Auftragsbearbeitung
- Existenz  eines Minimums bei Optimierungsproblemen

### Was bedeutet die "Eindeutigkeit" eines Modells?

Ein Modell ist eindeutig, wenn es genau eine Lösung gibt bzw. bei mehreren Lösungen eine präferierte Lösung gibt. Beispiele:
- globales Minimum
- stabile Lösung ohne Oszillation (Pseudostabile Zustände)

### Was bedeutet die "stetige Abhängigkeit von Eingabedaten" eines Modells?

Führen kleine Änderungen der Eingabedaten auch nur zu kleinen Änderungen der Lösung.

### Was sind andere Begriffe für die "stetige Abhängigkeit von Eingabedaten" eines Modells?

- Sensitivität
- Kondition

### Was ist laut Hadamard ein "sachgemäßes Problem" (well posed)? 

Ein Problem ist sachgemäß gestellt, wenn eine Lösung
- existiert
- eindeutig ist
- stetig von den Eingabegrößen abhängt

### Was ist ein Beispiel für "unsachgemäße Probleme" (ill posed)?

inverse Probleme: Ergebnis vorgegeben, Ausgangskonfiguration gesucht

### Wie werden "unsachgemäße" inverse Probleme gelöst?

- Lösen einer Folge von Vorwärtsproblemen bei Variation der Eingangsdaten (Optimierung)
- Regularisierung: Lösen eines sachgemäß gestellten, verwandten Problems

### Was bedeutet die "Verwendbarkeit" eines Modells?

Bewertet, ob ein Modell für die gewünschten Aussagen praxistauglich ist:
- Verfügbarkeit der Eingangsdaten in hinreichender Güte
- Existenz von schnellen Algorithmen zum Lösen des Modells (Speicher- und Laufzeitkomplexität)
- Lösung in gegebener Zeit findbar (Wettervorhersage für morgen muss vor morgen fertig sein)
- Konkurrenzfähigkeit gegenüber anderen Modellen (Preis-Leistungs-Verhältnis)
- vertretbarer Implementierungsaufwand

### Wie lassen sich Modelle klassifizieren?

- kontinuierlich vs. diskret
- deterministisch vs. stochastisch
- verwendete Skalen

### Was sind diskrete Modelle?

Modelle, die nur mit Ganzzahlen und Zustandsübergängen arbeiten

### Was sind kontinuierliche Modelle?

Modelle, die mit reellen Zahlen und allen Möglichen Zwischenzuständen arbeiten

### Was sind deterministische Modelle?

Systeme klassischer Differentialgleichungen ohne Zufallskomponente

### Was sind stochastische Modelle?

Modelle mit zufallsbehafteten Komponenten, zum Beispiel zur Modellierung von Turbulenz

### Was ist die "Multiskaleneigenschaft"?

Beeinflussen Phänomene auf kleiner Skala (z.B. winzige Turbulenzen) das Ergebnis auf großer Skala (Strömungseigenschaften eines Containerschiffs), muss das System sehr fein berechnet werden, um korrekte Ergebnisse auf großer Skala zu erhalten. Das führt aber zu nicht tragbarem Rechenaufwand.

### Welche Lösungsansätze gibt es zum Simulieren von Modellen?

- analytische Lösung
- heuristischer Lösungsansatz
- direkt numerischer Ansatz
- approximativ-numerischer Ansatz

### Was zeichnet die "analytische Lösung" aus?

- Lösung mit Bleistift und Papier
- keine Vereinfachungen / Näherungen nötig
- nur für einfache Systeme möglich

### Was zeichnet den "heuristischer Lösungsansatz" aus?

- Plausibilitätsargumente führen zu Lösungsstrategien
- in diskreter Simulation und Optimierung verwendet
- führen nicht zwingend zum besten Ergebnis
- Beispiel: Greedy-Algorithmen

### Was zeichnet den "direkt numerischer Ansatz" aus?

- Lösung bis auf numerischen Rundungsfehler genau
- Beispiel: Simplex-Algorithmus

### Was zeichnet den "approximativ-numerischer Ansatz" aus?

- Lösung erfolgt näherungsweise
- kontinuierliches Problem wird diskretisiert

### Was sind Kriterien zur Bewertung eines Simulationsergebnis?

- Validierung
- Verifikation
- Genauigkeit
- Kosten

### Welche Frage beantwortet die "Validierung"?

Werden die richtigen Gleichungen gelöst? (Wurde das korrekte Modell verwendet?)

### Welche Frage beantwortet die "Verifizierung"?

Werden die Gleichungen richtig gelöst? (Wurde das verwendete Modell korrekt gelöst?)

### Welche Möglichkeiten zur Validierung von Simulationsergebnissen gibt es?

- Abgleich mit Experimenten
- A posteriori Beobachtungen 
  - Realitätstest (insbesondere bei Vorhersagen)
  - Zufriedenheitstest (bei subjektiv bewerteten Ergebnissen, z.B. Computergrafik)
- Plausibilitätstests (theoretische Widersprüche zu geltenden Theorien)
- Modellvergleich (Vergleich mit anderer Simulation)

### Was sind die Nachteile vom Abgleich von Simulation mit Experimenten?

- leicht kleine Unterschiede zwischen Simulation und Messung
- Bei skalierten Modellen treten manche Effekte im kleinen nicht auf
- sporadische und systematische Messfehler

### Was ist Inhalt der Verifikation?

- Konvergenzbeweise der Algorithmen
- Korrektheitsbeweise für erstellte Programme
