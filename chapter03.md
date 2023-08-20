---
recall: header
---

### Was ist Spieltheorie?

mathematische Theorie, um Entscheidungssituation zu modellieren und Entscheidungsfindung abzuleiten

### Was ist ein "Spieler" in der Spieltheorie?

eine Person / Entität, die eine Entscheidung treffen muss

### Was ist eine "Strategie" in der Spieltheorie?

Handlungen, die ein Spieler ausführen kann

### Was sind zwei bekannte Beispiele für strategische Spiele?

- Gefangenendilemma
- Kampf der Geschlechter

### Was ist das Gefangenendilemma?

- Spiel der Spieltheorie
- zwei Verbrecher werden gefasst
- Schuld für einen Teil des Verbrechens ist bewiesen -> Mindeststrafe steht fest
- Jeder Verbrecher kann schweigen oder den anderen verraten
- schweigen beide, bekommen sie die Mindesstrafe
- schweigt nur einer, bekommt der Verräter Straferlass und der andere eine höhere Strafe
- schweigt keiner, bekommen beide eine höhere Strafe, allerdings niedriger als wenn nur einer
  schweigt

### Was ist der Kampf der Geschlechter?

- Koordinationsspiel mit Verteilungskonflikt
- zwei Spieler, zwei Orte, fehlende Abstimmung zum Treffpunkt
- die Vorlieben beider Spieler sind
  1. gemeinsam am Lieblingsort
  2. gemeinsam am anderen Ort
  3. einsam (Ort egal)
- die Lieblingsorte sind verschieden

### Wie werden die Strategien des anderen Spielers notiert?

Sei X der Spieler, dann bezeichnet $S_{-X}$ die Strategiemenge des anderen Spielers.

### Wann ist ein Spiel in der Spieltheorie "endlich"?

wenn die Strategiemengen aller Spieler endlich groß sind

### Wie bewertet ein Spieler den Nutzen seiner Strategie?

Auszahlungsfunktion, die gewählte Strategien (aller Spieler) auf eine reele Zahl abblildet

### Was ist die Nutzenmatrix?

Darstellung der Werte der Auszahlungsfunktion beider Spieler als Tupel in einer Matrix, die alle
Strategiekombinationen beinhaltet (auch: Auszahlungsmatrix)

### Woher stammt die Bezeichnungs "Zeilenspieler" und "Spaltenspieler"?

in Anlehnung an die Nutzenmatrix wählt der Zeilenspieler seine Strategie in den Zeilen der Matrix
und der Spaltenspieler in den Spalten.

### Was sind Nullsummenspiele?

Spiele bei denen der Wert der Auszahlungsfunktion bei einer Strategie für den "Gewinner" positiv und
für den "Verlierer" bei gleichem Betrag negativ ist

### Was sind "Gewinnspieler" und "Verlustspieler¨?

Spieler in einem Nullsummenspiel, der Gewinnspieler hat das positive Ergebnis, der Verlustspieler
das negative

### Was zeichnet die Nutzenmatrix eines Nullsummenspiels aus?

nur das Ergebnis eines Spielers ist eingetragen, weil das Ergebnis des anderen Spielers impliziert
ist (das negative des eingetragenen Werts)

### Was ist die "strategische Normalform" eines Spiels?

Darstellung des Spiels mittels Strategiemengen und Auszahlungsfunktion

### Was ist ein Spiel mit "vollständiger Information"?

Wenn allen Spielern die komplette Auszahlungsfunktion bekannt ist

### Was ist ein "Spiel bei Gewissheit"?

Ein Spieler weiß wie der andere entscheidet und kann seine Entscheidung entsprechend auf maximalen
Gewinn anpassen.

### Was ist ein "Spiel bei Risiko"?

Kein Spieler weiß wie der andere entscheidet und muss nur entsprechend seiner eigenen Mentalität
eine Strategie wählen.

### Welche Entscheidungsstrategien hängen nur von der Mentalität des einen Spielers ab?

Beim Spiel bei Risiko, also Ungewissheit über die Strategie des Gegenspielers:
- risikobereit: Spieler entscheidet sich für die Strategie mit maximalem Gewinn, auch wenn das
  maximalen Verlust bei ungünstiger Entscheidung des Gegenspielers bedeutet
- vorsichtig: Spieler entscheidet sich für die Strategie mit höchstem minimalem Gewinn

### Was beschreibt die "Reaktionsabbildung"?

bildet die Strategie des Gegenspielers auf die (davon abhängige) Strategie mit maximalem Gewinn in
der eigenen Strategiemenge ab (können mehrere sein)

### Warum bildet die Reaktionsabbildung auf die Potenzmenge der Stategiemenge eines Spielers ab?

weil zu einer Strategie des Gegenspielers mehrere Strategien aus der eigenen Menge optimal sein
können

### Wie lässt sich die Reaktionsabbildung in der Nutzenmatrix darstellen?

Für den Zeilenspieler wird in jeder Spalte der maximale Gewinn des Zeilenspielers durch
Unterstreichen markiert. Zeilen einer Spalte, die unterstrichene Werte beinhalten, sind Teil der
Reaktionsmenge.

### Was ist eine "dominante Strategie"?

Gibt es eine Strategie, die für jede Strategie des Gegenspielers das Optimum darstellt, ist es die
dominante Strategie.

### Was ist die dominante Strategie beim Gefangenendilemma?

beide gestehen

### Was passiert bei einem Spiel bei dem es nur für einen Spieler eine Dominante Strategie gibt?

Das Spieql reduziert sich zu einem Spiel mit Gewissheit, weil der Spieler ohne dominante Strategie
die dominante Strategie des Gegenspielers als ausgewählt annehmen kann, also einfach die beste dazu
passende Strategie wählt.

### Wie lassen sich Spiele ohne dominante Strategie im Umfang reduzieren?

Gibt es zwei Strategien, bei der die zweite für jede Strategie des Gegenspielers stets mindestens so
gut ist wie die erste, kann die erste aus dem Spiel gestrichen werden.

### Was ist ein "Nash-Gleichgewicht"?

ein Strategiepaar, bei dem die Strategie des einen Spielers die optimale Antwort auf die Strategie
des jeweils anderen ist, es gibt keinen Grund die Strategie zu wechseln

### Wie sind Nash-Gleichgewichte in der Nutzenmatrix erkennbar?

Zeichnet man die Reaktionsabbildung in die Nutzenmatrix ein (unterstreichen der jeweils besten
Reaktion auf jede Strategie des Gegners), so sind bei Nash-Gleichgewichten die Nutzen beider Spieler
unterstrichen.

### Wie wird ein Nash-Gleichgewicht in einem Nullsummenspiel auch genannt?

Sattelpunkt

### Was sind reine Strategien?

"normale" Strategien, also die vollständige Entscheidung für ein bestimmtes Vorgehen

### Was sind gemischte Strategien in der Spieltheorie?

Statt eine reine Strategie zu wählen, wird eine Wahrscheinlichkeit für eine Strategie gewählt. Über
eine geeignete Wahl der Wahrscheinlichkeiten ergibt sich im Erwartungswert der Nutzenmatrix ein
Nash-Gleichgewicht.

### Wie nennt man den Übergang von einem Spiel mit reinen Strategien zu einem mit gemischten Strategien?

gemischte Erweiterung

### Welche Vorteile bietet die mathematische Modellbildung in der Spieltheorie?

Problem aufs wesentliche reduziert -> besser analysierbar

### Mit welcher Tranformation der Nutzenmatrix wird die Strategie des vorsichtigen Spielers zu der des risikobereiten?

Wird maximaler Gewinn mit 0 bewertet und alle anderen Ausgänge ein Verlust gegenüber dem maximalen
Gewinn sind, wird der vorsichtige Spieler die Strategie wählen, die das geringste Potential für
Gewinneinbußen hat, was wiederum die Strategie mit maximalem Gewinn ist, also die risikobereite
Strategie des Ausgangsproblems.

### Was kann dazu führen, dass ein rational zu wählender Gleichgewichtspunkt nicht gewählt wird?

Rationale Entscheidungen gehen davon aus, dass beide Spieler rational handeln. Stellt ein Spieler
die Rationalität des Gegenspielers in Frage, können trotz eines offensichtlich optimalen
Gleichgewichts konservative Strategien gewählt werden, bei denen ein Abweichen des Gegenspielern für
den Spieler selbst zu nur geringen Verlusten führt.

### Was ist ein linearer Kongruenzgenerator?

ein einfacher Pseudozufallszahlengenerator

### Welche Parameter hat ein linearer Kongruenzgenerator?

- Seed, der erste Wert
- Faktor, wird mit der letzten generierten Zahl multipliziert wird
- Offset, der zum Produkt addiert wird
- Modulus, der die Summe teilt
