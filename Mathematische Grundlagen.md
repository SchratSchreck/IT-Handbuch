# Einführung in die Logik
In der Informatik ist die *formale Logik* die wichtigste Form der Logik. Die *Aussagenlogik* befasst sich mit der Verknüpfung und Wechselwirkung von Aussagen, Sätze die eindeutig wahr oder falsch sein können. Die Aussagenlogik wurde jedoch erst durch die Entwicklung der *Prädikatenlogik* von *Gottlob Frege* mathematisch nutzbar. Diese ist ein mathematisch-formale Schreibweise für Aussagen. Typische Formulierungen sind Satzanfänge mit *Quantoren*:
- *Ɐx, All-Quantoren:* "Für alle *x* gilt: ..."
- *Ǝx, Existenz-Quantoren:* "Es gibt (mindestens) ein *x*, für das gilt: ..."
## Aussagen
Aussagen können eindeutig wahr oder eindeutig falsch sein somit sind folgende Sätze Aussagen:
- Der Kölner Dom ist 157 Meter hoch.
- Der Kölner Dom ist 17 Meter hoch.
- Ich bin 17 Meter hoch.

Sätze wie die folgenden sind keine Aussagen, da sie Fragen sind oder subjektiv Meinungsäußerungen:
- Der Kölner Dom ist schön.
- Ist heute Freitag?
- Wie geht es dir?

Eine mathematisch Aussagen ist ein System aus *Termen* (mathematischen Ausdrücken), welche einfache numerische Konstanten, wie 100 oder -3,5, sein können, aber auch komplexe arithmetische Verknüpfungen, wie 3+5, welche erst in einen konkreten Wert aufgelöst werden müssen. 
Eine vollständige mathematische Aussage ist ein Vergleich zwischen zwei Termen, der folgende Formen annehmen kann:
- *Gleichung:* wahr, wenn beide Terme den gleichen Wert haben;
	  5+6 = 6+5
- *Ungleichung:* wahr, wenn beide Terme auf eine vorgegebene Weise unterschiedlich sind;
	  5+6 < 6+6
## Aussageformen
Verallgemeinerte Gleichungen mit Variablen sind keine Aussagen, da die Gleichung mit verschiedenen eingesetzten Variablen wahr oder falsch sein kann.
a+b=3
wahr: a = 2; b = 1 oder a = 3,5; b = -0,5
falsch: a = 3; b = 5 oder a = 0,75; b = 9

Ein Wert der eine *Aussageform* zu einer wahren Aussage macht ist Teil der *Lösungsmenge* der Aussageform. Diese Lösungsmenge kann aus keiner, einer, mehreren oder unendlich vielen Lösungen bestehen.
Die Lösungsmenge einer linearen Gleichung wird durch auflösen dieser bestimmt:
2x+7 = 21 |-7
<=> 2x = 14 |:2
<=> x = 7  => L = {x | x=7}
Die Lösungsmenge einer Ungleichung wird ebenfalls so bestimmt:
2x + 7 < 21 |-7
<=>2x < 14 |:2
<=> x < 7   => L = { x | x<7}

Eine wichtige Aussnahme von der Regel, dass Ausdrücke mit Variablen Aussageformen sind, ist, dass gemäß der Prädikatenlogik, Sätze Aussagen sind sofern alle Variablen quantifiziert werden:
-  Ɐx: x < x+1 (für alle x gilt, dass x kleiner als x+1 ist)
- Ǝx: x² = 4 (es gibt mindestens ein x, dessen Quadrat 4 ist (2 und -2))

## Logische Verknüpfungen
Das Fachgebiet der logischen Verknüpfungen nennt man *boolesche Algebra*, benannt nach dem englischen Mathematiker *Georg Boole*, welcher im 19.Jahrhundert eine Algebra der binären logischen Verknüpfungen entwickelte. 
Zu diesen logischen Verknüpfungen gehören:
- Schlussfolgerungen (Wenn-dann-Beziehungen)
- Und-Verknüpfungen
- Oder-Verknüpfungen

**Logische Schlussfolgerungen (Implikation)**
Eine Schlussfolgerung im sprachlichen Gebrauch kann sein:
1. Es regnet
2. Die Straße ist nass
	Es regnet => Die Straße wird nass 

Die direkte Umkehrung einer logischen Schlussfolgerung, wird *Kontroposition* genannt, jedoch muss man beachten, dass *A => B*, nicht die Kontraposition *B => A* bedingt. Sondern die verneinte Umkehrung: *-B => -A*. 
Diese zwei Formen werden:
- *Modus ponens ("setzender Modus")*
	Gegeben: A => B
	Feststellung: A ist wahr
	Schlussfolgerung: Also ist auch B wahr
- *Modus tollens ("wegnehmender Modus")*
  Gegeben: -B => -A
  Feststellung: B ist nicht wahr 
  Schlussfolgerung: A ist nicht wahr

| Schlussfolgerung | Beispiel                                                       | Kontraposition | Beispiel                                                |
| :--------------: | :------------------------------------------------------------- | :------------: | :------------------------------------------------------ |
|      A => B      | Wenn es regnet, wird die Straße nass.                          |    -B => -A    | Wenn die Straße nicht nass wird regnet es nicht.        |
|     A => -B      | Wenn die Sonne schein, ist es nicht Nacht.                     |    B => -A     | Wenn es Nacht ist, scheint nicht die Sonne.             |
|     -A => B      | Wenn ich nicht frei habe, muss ich arbeiten.                   |    -B => A     | Wenn ich nicht arbeiten muss, habe ich frei.            |
|     -A => -B     | Wenn ich keinen Führerschein habe, darf ich nicht Auto fahren. |     B => A     | Wenn ich Auto fahren darf, habe ich einen Führerschein. |
Implikationen sind nicht alle gleich stark, sondern es wird unterschieden zwischen:
- *hinreichend:* Wenn die Bedingung auftritt, führt dies immer dazu, dass die Wirkung eintritt. Jedoch kann es auch andere Ursachen für die Wirkung geben. (A => B)
  "Wenn es regnet ist es eine *hinreichende* Bedingung, dass die Straße nass wird."
- *notwendig:* Die Wirkung kann nicht ohne die Bedingung auftreten, jedoch ist die Bedingung nicht alleine für die Wirkung ausreichend. (-A => -B; B => A)
  "Damit eine Lampe leuchtet ist ein geschlossener Stromkreis *notwendig*, aber die Lampe darf auch nicht defekt sein." 
- *hinreichend und notwendig:* Nur diese eine Bedingung allein führt zu der einen bestimmten Wirkung.
  "Nur wenn eine Zahl ohne Rest durch 2 teilbar ist, ist sie eine gerade Zahl"

>[!info] Korrelation
>Wenn etwas weder *hinreichend* noch *notwendig* ist, ist es keine Bedingung. Sollte jedoch ein Ereignis A statistisch relativ häufig vor oder zusammen mit einem Ereignis B auftretten  spricht man von einem *Zusammenhang* oder auch *Korrelation*.


**Und-Verknüpfungen (Konjunktion)**
Wenn mehrere Bedingungen durch *Und (∧)* verknüpft werden, ergibt sich nur eine wahre Aussage, wenn alle Bedingungen wahr sind.
- "Wenn die Glühbirne funktioniert *und* der Lichtschalter eingeschalten ist, dann leuchtet das Licht."

Logische Verknüpfungen werden in vielen Programmiersprachen durch `&&` dargestellt.

>[!info] Wahrheitstabellen
>*Wahrheitstabellen* werden benutzt um Verknüpfungen darzustellen, wobei wahre Aussagen durch eine 1 und unwahre Aussagen durch ein

|     |     |     |
| :-: | :-: | :-: |
|  ∧  |  0  |  1  |
|  0  |  0  |  0  |
|  1  |  0  |  1  
**Oder-Verknüpfungen (Disjunktion)**
Werden mehrere Aussagen durch ein *Oder (∨)* verknüpft, ergibt sich eine wahre Aussage, wenn mindestens eine Teilaussage wahr ist. 
- "Wenn ich eine Millionen Euro im Lotto *oder* in einer Quizsendung gewinne, dann bin ich Millionär."

Oder-Verknüpfungen werden in vielen Programmiersprachen durch `|`, für bitweise Verknüpfung, oder durch `||`, für logische Verknüpfungen, dargestellt.

|     |     |     |
| :-: | :-: | :-: |
|  ∨  |  0  |  1  |
|  0  |  0  |  1  |
|  1  |  1  |  1  |
>[!info] Logsiche und Bitweise Verknüpfungen
>Computer können logische Verknüpfungen auf zwei Arten nutzen:
>- *logische Verknüpfungen:* hier wird eine klassische Bedingungsprüfung durchgeführt; ein Programm soll einen Schritt nur durchführen, wenn ein Bedingung zutrifft.
>- *bitweise Verknüpfungen:* hier werden einzelnen Bits verknüpft, z.B. 
>  `0110 ∨ 1100 => 1110` 

>[!info] De-Morgan-Theoreme
>Die, nach dem britischen Mathematiker Augustus de Morgan benannten, Äquivalenzen müssen vor allem beim Programmieren von verknüpften "Wenn-dann-Bedingungen" beachten.
>-A ∧ -B <=> -(A ∨ B)
>-A ∨ -B <=> -(A ∧ B)

**Rechengesetze**
Bei logischen Verknüpfungen gelten die Rechengesetze, wobei die Umformung logischer Sätze als *logisches Kalkül* bezeichnet wird:
- *Kommutativgesetz:*
  A ∧ B = B ∧ A
  A ∨ B = B ∨ A
- *Assoziativgesetz:*
  (A ∧ B) ∧ C = A ∧ (B ∧ C)
  (A ∨ B) ∨ C = A ∨ (B ∨ C)
- *Distributivgesetz:*
  A ∧ (B ∧ C) = (A ∧ B) ∧ (A ∧ C)
  A ∨ (B ∨ C) = (A ∨ B) ∨ (A ∨ C)
- *Neutralitätsgesetz:* 
  (neutrales Element *A*, kann 0 oder 1 sein)
  A ∧ 1 = A
  A ∨ 0 = A

**XOR-Verknüpfung**
Bei der *exclusive OR (XOR)*-Verknüpfung, ergibt sich eine wahre Aussage, wenn genau eine Teilaussage wahr ist.
- "Wenn ich entweder mit dem Fahrrad oder dem Auto fahre, gelange ich rechtzeitig zur Arbeit." (Ich kann nicht gleichzeitig mit dem Auto und dem Fahrrad fahren.)

In Programmiersprachen der C-Tradition gibt es die XOR nur zur bitweisen Verknüpfung mit dem Symbol `^`.
Die XOR-Verknüpfung kann man auch simulieren:
- A XOR B = (-A ∧ B) ∨ (A ∧ -B)

|     |     |     |
| :-: | :-: | :-: |
| XOR |  0  |  1  |
|  0  |  0  |  1  |
|  1  |  1  |  0  |
**XNOR-Verknüpfung (Äquvalenz)**
Bei der XNOR-Verknüpfung, ergibt sich eine wahre Aussage, wenn beide Teilaussagen den gleichen Wert haben.

|      |     |     |
| :--: | :-: | :-: |
| XNOR |  0  |  1  |
|  0   |  1  |  0  |
|  1   |  0  |  1  |
## Mengenoperationen
Eine Menge ist eine Gruppe aus unterschiedlichen Werten, die entweder als Abfolge einzelner Zahlen oder durch Regeln definiert wird:
- M := {1,2,3,...}
- N  := {x |x < 10 ∧ x ∈ ℝ} (x ist kleiner als 10 und Element der reelen Zahlen)

**Beziehungen zwischen Mengen und einzelnen Werten**
Ein Wert ist *Element* einer Menge, wenn er in ihr vorkommt.
Ein Wert ist nicht Element einer Menge, wenn er nicht in ihr vorkommt.
M := {3,4,5}
- 3 ist Element von M; 3 *∈* M
- 2 ist kein Element von M; 2 *∉* M

P := {x |x < 5 ∧ x ∈ ℝ}
- Alle Zahlen die kleiner als 5 sind und zu den reelen Zahlen gehören sind Elemente der Menge P

Die Anzahl der Elemente einer Menge, nennt man *Kardinalität* oder *Mächtigkeit* einer Menge. Mengen können endlich viele Elemente haben aber auch unendlich viele. Bei einer unendlichen Menge ist, jedoch wichtig, dass man unterscheiden muss zwischen:
- *abzählbar unendlichen:* die Menge kann mit den natürlichen Zahlen abgezählt werden
- *überabzählbar:* die Menge hat eine größere Mächtigkeit als die natürlichen Zahlen

**Beziehungen zwischen Mengen**
Eine Menge M heißt *Teilmenge* einer Menge N, wenn jedes Element von M auch eine Elemente von N ist. 
Eine Menge M ist keine Teilmenge einer Menge N, wenn mindestens ein Element von M kein Element von N ist.
M := {3,5,6,7}
N := {2,5,6,7}
P := {3,5,6,7,8}
- M ist eine echte Teilmenge von P: M ⊂ P
- N ist keine Teilmenge von P: N ⊄ P

>[!info] (echte) Teilmenge und (echte) Obermenge
>Man spricht von einer *echten Teilmenge  `⊂`* nur dann, wenn gilt:
>- Für jedes x ∈ M, auch x ∈ N
>- mindestens ein Element aus N, x ∈ N, dass nicht in M ist x ∉ M
>Ist M eine echte Teilmenge von N, M ⊂ N, dann ist N die *echte Obermenge `⊃`* von M, N ⊃ M.
>
>M kann auch dann eine Teilmenge sein, wenn M und N identisch sind, M = N. Ist das der Fall dann wird `⊆`, "Teilmenge oder gleich", und `⊇`, "Obermenge oder gleich" benutzt:
>- M ⊆ N und N ⊇ M
>

**Verknüpfung von Mengen**
- **Schnittmenge ∩**
  Die Schnittmenge M ∩ N, beinhaltet die Elemente die in beiden Mengen vorhanden ist:
  M = {2,3,4}
  N = {4,5,6}
  M ∩ N = {4}
  Gibt es keine Schnittmenge wird es so dargestellt:
  P ∩ Q = {} = ∅
- **Vereinigungsmenge ∪**
  Die Vereinigungsmenge M ∪ N, beinhaltet alle Elemente von M und N:
  M = {2,3,4}
  N = {4,5,6}
  M ∪ N = {2, 3, 4, 5, 6}
- **Differenzmenge ∖**
	Die Differenzmenge (Komplement oder Restmenge) M ∖ N, beinhaltet alle Elemente die in M aber nicht in N vorhanden sind:
	M = {2, 3, 4}
	N = {4, 5, 6}
	M ∖ N = {2, 3}

**Rechengesetze**
Auch bei Mengenoperationen gelten die Rechengesetze
- *Kommutativgesetz:*
  A ∩ B = B ∩ A
  A ∪ B = B ∪ A
- *Assoziativgesetz:*
  (A ∩ B) ∩ C = A ∩ (B ∩ C)
  (A ∪ B) ∪ C = A ∪ (B ∪ C)
- *Distributivgesetz:*
  A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C)
  A ∩ (B ∪ C) = (A ∪ B) ∩ (A ∪ C)


>[!info] Zahlenmengen der Mathematik
>1. *Die Natürlichen Zahlen ℕ*
>   Alle Zahlen mit denen sich Anzahlen ausdrücken lassen:
>   ℕ = {1,2,3,4,...}
>   Die natürlichen Zahlen sind eine abzählbar unendliche Menge.
>   In der klassichen Mathematik ist die 0 kein Element von ℕ, falls sie zusätzlich enthalten ist wird das Symbol ℕ₀ benutzt.
>   DIN-Norm 5473 schreibt jedoch vor, dass 0 in ℕ enthalten ist, falls sie nicht enthalten ist wird das Symbol ℕ* benutzt.
>2. *Die Ganzen Zahlen ℤ*
>   Die ganzen Zahlen sind, wie die natürlichen Zahlen, keine Bruchzahlen, jedoch beinhalten sie die 0 und negative Zahlen. Die ganzen Zahlen sind abzählbar unendlich.
>   ℤ = {..., -2, -1, 0, 1, 2, ...}
>3. *Die Rationalen Zahlen ℚ* 
>   In dieser Menge kommen auch Dezimalbrüche, Zahlen die durch die Division zweier ganzer Zahlen gebildet werden, hinzu.
>   Die rationalen Zahlen sind abzählbar unendlich, da sich alle Brüche in eine abzählbare Reihenfolge bringen lassen.
>   Die Definition der rationalen Zahlen:
>   ℚ = {x |x = p/q ∧ p ∈ ℤ ∧ q ∈ ℤ ∧ q ≠ 0}
>4. *Die Reellen Zahlen ℝ*
>    Die reelen Zahlen fügen nun auch periodische Zahlen, Zahlen mit unendlich vielen Nachkommastellen, hinzu. 
>    Beispiele sind die Kreiszahl π (3,1415926...), die eulerische Zahl e (2,718281828...), die Basis des natürlichen Logarithmus, oder √2 (1,41421356...).
>    Die reelen Zahlen sind überabzahlbar unendlich.
>    Die Definition der reelen Zahlen:
>     ℝ = {x |x² ⋝ 0}
>     Die reelen Zahlen und periodische Dezimalbrüche lassen sich nicht in Computern darstellen, da diese eine feste Anzahl von Bits zur Darstellung von Zahlen verwenden, können die unendlichen Nachkommastellen nur mit einer bestimmten Genauigkeit dargestellt werden.
>5. *Die Komplexen Zahlen ℂ*
> 	  Hier kommen zusätzlich die *imaginären Zahlen* hinzu. Diese werden benutzt um die Wurzel negativer Zahlen zu berechnen. Dafür wird der *Imaginärteil i* als Lösung der Gleichung *i² = -2* eingeführt und jede imaginäre Zahl ist als Summe des Imaginärteils i und einem *Realteil (reelen Zahl)* definiert.
> 
> Es zeigt sich also folgende Beziehung zwischen den Zahlenmengen:
> ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ ⊂ ℂ 
> ℂ ⊃ ℝ ⊃ ℚ ⊃ ℤ ⊃ ℕ

## Folgen und Reihen
*Zahlenreihen* sind (abzählbar unendliche) Abfolgen von Zahlen, die nach bestimmten Formeln gebildet werden. Die Zahlen werden durch einen Index (x₁, x₂, x₃, ...).
Die einfachste Zahlenfolge sind die natürlichen Zahlen mit der Formel:
- xₙ = n (x₁ = 1, x₂ = 2,...)

Auch arithmetsiche Operationen können teil einer Formel sein:
- xₙ = n² = 1, 4, 9, 16,... 

Desweiteren können auch mehrere Formeln für eine Zahlenfolge gelten:
- xₙ = 
  n-1 f. n < 3; 
	n+1 f. n ≥ 3 ; 
	=> 0,1,4,5,...

Wichtige Eigenschaften die Folgen haben können sind:
- *monton steigend:*
  für jedes Element gilt xₙ ≥ xₙ₋₁; jedes Element ist größer als oder gleich dem Vorherigen
- *streng monoton steigend:*
  für jedes Element gilt xₙ > xₙ₋₁; jedes Element ist größer als das Vorherige
- *monoton fallend:*
  für jedes Element gilt xₙ <= xₙ₋₁; jedes Element ist kleiner als oder gleich dem Vorherigen
- *streng monoton fallend:*
  für jedes Element gilt xₙ < xₙ₋₁; jedes Element ist kleiner als das Vorherige
- *bijektive Abbildung / Bijektion:*
  streng monotone Folgen sind immer abzählbar unendlich, da genau einem Element aus der Folge ein Element aus ℕ zugeordnet werden kann; die nennt man auch *eindeutig*
- *Injektiv:*
	monotone Folgen sind *injektiv*, da zwar jedem Element aus ℕ ein Element aus der Zahlenfolge zugeordnet werden kann; jedoch kann nicht jedem Element eindeutig ein Element aus ℕ zugeordnet werden kann
	z.B.: x₁ = 1,... x₆ = 1
- *konstant:*
	jedes n hat den selben Wert
	z.B.: xₙ = 1 = 1,1,1,1,...	
- *alternierend:*
  Das Vorzeichen ändert sich abwechselnd bei jedem Element
  z.B.: 1, -1, 2, -2,...
- *beschränkt:*
  Eine Folge ist beschränkt, wenn sie sich zwischen einer *unteren Schranke s* und *obernen Schranke S* bewegt
  z.B.: xₙ = sin n => s = -1, S = 1

**Limes**
Wenn eine Zahlenfolge sich einem Wert immer mehr nähert, diesen aber nicht erreicht ,sondern ins (Negativ) Unendliche schießt oder beginnt sich zu alternieren, heißt dieser Wert *Grenzwert* oder *Limes*. 
Dies wird mathematisch folgend dargestellt:
- z.B.: $\lim_{ n \to \infty} (\frac{1}{n}) = 0$
Gesprochen bedeutet diese Formel: "Der Limes von 1/n für n gegen unendlich ist 0."
Folgen mit Grenzwert nennt man *konvergent*, während Folgen ohne Grenzwert *divergent* heißen.

**Reihen**
Eine *Reihe* besteht aus Elementen mit Index, die durch arithmetische Operationen zusammengefasst. Dabei gibt es zwei verschiedene Reihen:
1. *Summenreihe:* mit dem Symbol  `Σ` geschrieben:
   - $\sum_{i=1}^n xᵢ = x₁ + x₂ +...+xₙ$
   - z.B.: $\sum_{i=1}^{10} i^2 = 1² + 2²+3²+\dots+100=385$

2. *Produktreihe:* mit dem Symbol `Π` geschrieben:
   - $\prod_{i=1}^n x_{1}$ 
   - z.B. $6! = \prod_{i=1}^6 = 1 \cdot 2 \cdot 3 \cdot 4 \cdot 5 \cdot 6 = 720$
# Dreisatz
Der Dreisatz dient zur Umrechnung von Verhältnissen, bei der ein Verhältnis zwischen zwei Werten bekannt ist und ein dritter gegeben, woraus man den vierten Wert berechnen kann.
Als Gleichung:
$$
\frac{a}{b} = \frac{c}{x} \implies x = \frac{b \cdot c}{a}
$$

Als Beispiel: 25 m Kabel kosten 13,95. Wie viel kosten 45m?
$$
\frac{25}{13,95} = \frac{45}{x} \implies x = \frac{13,95 \cdot 45}{25}
$$

# Lösen von Gleichungssystemen
**Lineare Gleichungen**
Das einfachste Verfahren zum Lösen von Gleichungen ist das *Einsetzverfahren*, bei der eine Gleichung nach einer Variabel aufgelöst wird und der Wert hinter dem Gleichheitszeichen wird anstatt der Variabel in eine andere Gleichung eingesetzt.

$$ \begin{align} 
Ⅰ.x+y = 7 \\
Ⅱ. 2x - y = 2\\
\text{Ⅰa in Ⅱ:} \\
 2x -(7-x) =2\\
\Leftrightarrow 2x -7+x =2 \\
\Leftrightarrow 3x-7=2 \\
\Leftrightarrow 3x=9 \\
\Leftrightarrow x = 3 \\
\text{x in Ⅰ. einfügen} \\
x+y=7 \\
3 + y = 7 \\
y=4 \\
\text{L = {3,4}}
\end{align} $$

**Gleichungen höheren Grades (Polynome)**
Bei der Lösung von Polynomen, bei denen die Unbekannte die Basis einer Potenz bildet und der Grad die höchste in der Gleichung vorkommende Potenz angibt. 
Das bekannteste Lösungsverfahren zur Lösung  *quadratischer Gleichungen* (Polynom zweiten Grades; *ax² + bx + c = d*) ist die *pq-Formel*. 
Um die pq-Formel anzuwenden muss man die Gleichung erst in die *Normalform* (*x² + px + q = 0*) umwandeln:
- ax² + bx + c = d => x² + px + q = 0
- z.B.: 2x² -2x + 8 = 4:
	=> 2x² - 2x + 4 = 0
	=> x² - x + 2 = 0
 Die pq-Formel lautet:​​
$$ 
x_{1/2} = -\frac{p}{2} ± \sqrt{\left( \frac{p}{2}^2 \right)-q }
$$
Wenn das Ergebnis der Addition und Subtraktion unterschiedlich sind hat die Gleichung zwei Lösungen, sind die Ergebnisse identisch hat die Gleichung eine Lösung und sollte unter der Wurzel eine 0 oder negative Zahl stehen, keine Lösung. 
# Stochastik
## Wahrscheinlichkeitsrechnung
Die Wahrscheinlichkeitsrechnung ermittelt die *Wahrscheinlichkeit*, also die durchschnittliche Häufigkeit eines Ergebnis. 
Die Häufigkeit kann dabei als:
-  *absolute Häufigkeit:* die absolute Anzahl an Ergebnissen und wird durch natürliche Zahlen dagestellt
- *relative Häufigkeit:* die Häufigkeit der Ergebnisse im Verhältnis zu allen möglichen Ergebnissen; wird als Dezimalzahl oder Bruch angegeben wird; 1 bedeutet, dass das Ergebnis immer zutrifft, 0, dass das Ergebnis nie eintritt; (probabiltity) P = $\frac{x}{y}$
Faire Zufalls-Experimente, bei denen alle Ergebnisse die gleiche Wahrscheinlichkeit haben aufzutreten heißen *Laplace-Experimente*
**Beispiele**
- Münzwurf: zwei mögliche Ergebnisse, Kopf oder Zahl; P(K) = $\frac{1}{2}$ 
- Würfelwurf: sechs mögliche Ergebnisse, P(x)=$\frac{1}{6}$ 

Gegenstand von Berechnungen in der Wahrscheinlichkeitsrechnung ist die Kombination von mehreren Ergebnissen oder Experimenten.
- Die Wahrscheinlichkeit für eine *Kombination von Ereignissen* wird *addiert*:
  z.B. Die Wahrscheinlichkeit eine gerade Zahl (2,4,6) zu würfeln: $\frac{1}{6} + \frac{1}{6}+\frac{1}{6} = \frac{1}{2}$ 
- Die Wahrscheinlichkeit eines *bestimmten Ereignisses aus mehreren Experimenten* wird *multipliziert*:
  z.B. Die Wahrscheinlichkeit mit zwei Würfeln die gleiche Zahl zu würfeln: $\frac{1}{6} \cdot \frac{1}{6}= \frac{1}{36}$

**Ziehen aus einer Urne**
Die meisten Zufallsexperimente lassen sich auf das Experiment 
"Ziehen (verschiedenfarbiger) Kugeln aus einer Urne" abstrahieren. Dabei werden mehrere Kugeln aus einer Urne gezogen und entweder wieder zurückgelegt oder draußen gelassen.

## Statistik
Die Aufgabe der *Statistik* ist es die Ergebnisse von Messungen, Zählungen und anderer Datenerhebungen zu untersuchen und vergleichbar zu machen. 
Die *Prozentrechnung* wird benutzt um verschiedene Werte in ein Verhältnis miteinander 
zusetzen:
**Beispiel**
In Gemeinde A wohnen 3.500 Menschen, in Gemeinde B 5.000. In zwei aufeinanderfolgenden Jahren hat sich die Anzahl  der Fahrradfahrer folgend verändert:

| Gemeinde | Jahr 1 | Jahr 2 |
| -------- | ------ | ------ |
| A        | 670    | 850    |
| B        | 1.100  | 1.300  |
Um diese Werte Vergleichen zu können werden sie in einen Prozentsatz umgerechnet und in ein Verhältnis zu 100 gesetzt:
- Gemeinde A: 
  Jahr 1: $\frac{670}{3500} =\frac{x}{100} ⇔ x=\frac{670}{3500}\cdot 100 ≈ 19,14\%$
- Gemeinde B:
  Jahr 1: $\frac{1.100}{5.000} = \frac{x}{100} ⇔x = \frac{1.100}{5.000} \cdot 100 ≈ 22\%$ 

Daraus ergeben sich folgende Ergebnisse

| Gemeinde | Jahr 1 | Jahr 2 |
| -------- | ------ | ------ |
| A        | 19,14% | 24,29% |
| B        | 22%    | 26%    |
Um den prozentualen Zuwachs zu errechnen wird der Wert aus dem ersten Jahr als 100% betrachtet wird. Damit wird 100 sich zu 19,14 im gleichen Verhältnis wie 24,29 zu dem gesuchten Zuwachs:
- $\frac{100}{19,14} = \frac{x}{24,29} ⇔ x= \frac{100}{19,14} \cdot 24,29 ≈ 126,91$ 
Im zweiten Jahr beträgt die Fahrradnutzung 126,91% im Vergleich zum ersten Jahr, also ein Zuwach von 26,91%.

**Deskriptive Statistik**
Die Berechnungen der *deskriptiven Statistik* werden auf Datenreihen angewendet um Aussagen über diese treffen zu können.
Beispiel Außentemperatur:

| Mo   | Di   | Mi   | Do   | Fr   | Sa   | So   |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 21°C | 18°C | 19°C | 14°C | 16°C | 20°C | 21°C |
Um diese Werte zu untersuchen:
1. Die Werte werden der Größe nach sortiert:
   14, 16, 18, 19, 20, 21, 21
2. Wir haben nun xₘᵢₙ = 14 und xₘₐₓ = 21; Die *Spannweite R* beträgt R = xₘₐₓ - xₘᵢₙ = 7
3. Der *Mittelwert* oder *arithmetisches Mittel* wird folgend berechnet:
   $$
x̄ = \frac{1}{n} \sum_{i=1}^{n} x_{i} = \frac{x_{1} + x_{2} + \dots x-_{n}}{n}
$$
Also:
 $$
x̄ = \frac{1}{7} \sum_{i=1}^{7} x_{i} =  \frac{14+16+18+19+20+21+21}{7}= \frac{129}{7}= 18,43
$$
>[!info] 
>Das arithmetische Mittel ist ein linearer Durchschnitt und kann daher nur für lineare Wertereihen und Summenreihen benutzt werden.


In einer Datenreihe mit "Ausreißer" kann man den mittleren Wert mit dem *Median x̃* berechnen:
1. Die Werte nach der Größe sortieren:
   17, 33, 35, 35, 36, 37, 38
   14, 16, 18, 19, 20, 35
2. Bei einer Datenreihe mit *ungerader Anzahl* ist das Element an der Stelle $\frac{n+1}{2}$:
   $\frac{8}{2}=4$ => 35
3. Bei einer Datenreihe mit *gerader Anzahl* das Ergebnis aus den zwei Werten um die Mitte
   $\frac{1}{2}\cdot (x \frac{n}{2} + x (\frac{n}{2}{+1}$)):
   $\frac{1}{2} \cdot \left( x \frac{6}{2} + x \left( \frac{n}{2}+1 \right) \right) = \frac{1}{2} \cdot (18+19) = 18,5$ 

Der *Modus x̄* gibt den am häufigsten vorkommenden Wert in einer Datenreihe an: x̄ = 35

*Varianz* und *Standardabweichung* werden als Maße für die Wertestreuung benutzt, und auch um Daten durch statistische Berechnungen in Gruppen einzuteilen.
Die *Varianz* einer Datenreihe wird folgend berechnet:
$$
Var(X) = \frac{1}{n-1} \cdot \sum_{i=1}^{n} (x_{i} - x̄)²
$$
- 14, 16, 18, 19, 20, 21, 21
  $\frac{1}{6} \cdot ((14-18,43)²+ \dots + (21-18,43)²) ≈ 6,95$

Die *Standardabweichung σ* ist die Quadratwurzel der Varianz und wird oft verwendet, da die Varianz ein falschen falschen Eindruck der Verhältnisse macht und die dort im Quadrat gesetzten Werte wieder dem Original entsprechen:
$σ = \sqrt{ 6,95 } ≈ 2,64$

Bei *Produktreihen* wird das *geometrische Mittel* benutzt:
$$
x̄_{geom} = \sqrt[n]{ \prod_{i=1}^{n}{x_{i}} }
$$
# Lineare Algebra
**Vektoren**
Ein *Vektor* ist eine Strecke mit einer bestimmten Richtung in einer Ebene, Raum oder höheren Dimensionen, sogenannte *Vektorräume*.
- Zweidimensionale Vektoren im Vektorraum *ℝ²* (der Ebene):
  $$
\vec{v} = \begin{pmatrix}
x \\
y
\end{pmatrix}
$$
- Dreidimensionale Vektoren im Vektorraum *ℝ³*:
  $$ \vec{v} =
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
$$

Zweidimensionale Vektoren werden grafisch als Pfeile in einem kartesischen Koordinatensystem dargestellt. Dabei beschreiben die Werte des Vektors die Ausdehnung in Richtung der x- und y-Achse.
