#1-Einführung
**Die Maschinensprache des Prozessors**
Mirkoprozessoren verstehen nur *Maschinensprache*, bestehend aus Zahlen, welche Befehle und Argumente darstellen. Maschinensprache ist für den Menschen unleserlich und in normalen Text-Editoren als "Zeichensalat" dargestellt. Sollte man Maschinensprachendateien von Hand modifizieren müssen sollte man einen *Hex-Editor* benutzen.

**Assembler**
Assembler wurde entwickelt um Maschinensprache für den Menschen benutzbar zu machen, indem die Befehle nicht als Zahlencodes sondern als Kürzel dargestellt werden. Die Befehle selber werden vom Prozessorhersteller festgelegt und sind für jede Prozessor-Architektur unterschiedlich.

Das Assembler Programm beherrscht auch die Definition von *Makros*, Abfolgen von Befehlen die die unter einem eindeutigen Namen abgespeichert und wieder aufgerufen werden können.
Assembler wird heutezutage nicht mehr zum Schreiben vollständiger Programme benutzt jedoch oft in sehr hardwarenahen Prozessen wie etwa:
- In hardwarenahen Kernroutinen von Betriebssystemen, damit der Rest des Systems in einer höheren Sprache, oft C, geschrieben werden kann. (Wurde in den 70er bei der Implementierung von Unix eingeführt und ist immernoch aktuell.)
- Gerätetreiber 
- In der Spieleprogrammierung, besonders von schnellen 3D Spielen
- Systemnahe Computerviren

**Höhere Programmiersprachen (Fortan, Cobol, Basic)**
Mitte der 50er Jahren wurden problem- und benutzerorientierte Programmiersprachen eingeführt, die die maschinenorientierten Sprachen ablösten. 
Diese Programmiersprachen müssen erst in Maschinensprache übersetzt werden, deswegen wurden zwei Vorgehensweisen entwickelt:
- *Compiler:* erzeugt ein dauerhaft lauffähiges Machinensprachenprogramm und speichert es als ausführbare Datei (*Binary Executable*)
- *Interpreter:* der Quellcode eines Programms wird Zeile für Zeile während der Laufzeit übersetzt 
> [!note] Moderne Mischformen von Interpretern und Compilern
> Compiler übersetzten heute oft den Code nicht in Binärcode eines Prozessors, sondern in Bytecode einer virtuellen Maschine, die auf verschiedener Hardware ausgeführt werden kann.
> 
> Auch kommen werden Skriptsprachen häufig durch *Just-in-Time-Compiler* vor der Ausführung komplett übersetzt, statt während der Laufzeit, wobei der Bytecode im Cache zwischengespeichert wird.

Die Programmiersprachen hatten einen speziellen Verwendungszweck:
- *Fortan:* Abkürzung von "Formula Translator"; speziell für mathematische Bedürfnisse entwickelt; in Mathematik und Ingenieurwissenschaften heute noch verwendet
- *Cobol:* Abkürzung von "Common Business-oriented Language"; entwickelt für Handel und Wirtschaft
- *Basic:* Abkürzung von "Beginner's All-Purpose Symbolic Instruction Code"; einfache Sprache für Anfänger;  weit verbreitet als sie in den 70ern von Microsoft für Personal Computers angepasst wurde; in den 80ern in fast jeder ROM von Home Computern eingebaut

**Imperative und prozedurale Programmiersprachen (Pacal, C)**
Diese Programmiersprachen erlaubten eine *Strukturierung* und *Modularisierung* von Programmen, wodurch Programme in kleinere, logische und wiederverwendbaren Einheiten eingeteilt werden konnten, sogenannte *Prozeduren* oder *Funktionen*.
- *Pascal:* wurde 1968 vom Schweizer Mathematikprofessor Niklaus Wirth, als Lehrsprache entwickelt und ist noch heute als Lehrmittel beliebt.
- *C:* wurde 1971 von *Dennis Ritchie* und *Brian Kernighan* bei AT&T um eine portierbare Version von *Unix* zu schreiben. Da sie ursprünglich für den Computer DEC PDP-7 geschrieben wurde hat sie ähnliche Fähigkeiten wie Assembler, ist aber benutzerfreundlicher.
Das wegefallene Kapitel über die C Programmierung kann man [hier](https://github.com/SaschaKersken/ITHandbuch10/blob/main/docs/programmiersprache_c.pdf) finden.

**Objektorientierte Programmiersprachen (Smalltalk, C++, Java, C#)**
Im Zentrum von objektorientierten Programmiersprachen steht die *Klasse*, ein wiederverwendbares "Paket", die zur Konstruktion von *Objekten* verwendet wird. Diese haben *Funktionen*, durch welche sie "agieren" können.
Die wichtigsten Vorteile der OOP sind:
- *Kapselung:* Datenstrukturen können nicht von außerhalb der Klasse direkt auf dessen innere Daten zugreifen, sondern nur auf deren Methoden
- *Vererbung:* Klassen können ihre Eigenschaften und Methoden "Kindklassen" vererben, dadurch müssen nur die Unterschiede programmiert werden. 

Zu den wichtigsten objektorientierten Programmiersprachen gehören:
- *Smalltalk:* erste vollständige objektorientierte Sprache; in den 70er Jahren zur GUI-programmierung entwickelt
- *C++:* objektorientierte Erweiterung von C; entwickelt von *Bjarne Stroustrup*; abwärtskompatibel mit C, kann gemischt verwendet werden
- *Java:* benutzt eine *Java Virtual Machine (JVM)* in der das kompilierte Progamm läuft, wodurch es plattformunabhängig ist 
- *C#:* entwickelt von Microsoft zur Anwendungsentwicklung für das .NET Framework

**Logische und funktionale Programmiersprachen (LISP, Prolog, Logo)**
Der Ansatz dieser Programmiersprachen ist nicht einen fertigen Algorithmus zu schreiben und diesen mit verschiedenen Wertbelegungen vom Computer berechnen zulassen, sondern das Grundproblem zu formulieren und eine möglichst optimale Lösung vom Compiler erzeugen zu lassen.
Wegweisend in der Entwicklung dieser Programmiersprachen waren die Arbeiten von *Noam Chomsky*. Dieser stellte eine Verbindung zwischen Sprachwissenschaften und Informationstechnik her und entwickelte basierend auf dieser sogenannte *Expertensysteme*. Diese beantworten Fragen durch logische Schlussfolgerungen aus bereits bekannten Informationen. Logische Programmiersprachen waren bei der Implementierung solcher Systeme ideal.
Logische Programmiersprachen benutzen *Prädikatenlogik* zur Formulierung von Ausdrücken und Termen; der wichtigste Vertreter ist *Prolog*.

Sprachen die lediglich eine andere Syntax haben werden auch *funktionale Sprachen* bezeichnet. Hierzu gehören *LISP* und *Logo*, welche Entwickelt wurden um Kindern die Denkweise von Computern beizubringen. Als Oberbegriff kann auch *deklarative Programmiersprache* verwendet werden.

Bei der Programmierung von modernen Mehrkernprozessoren eignen sich logische und funktionale Sprachen sehr gut, weswegen sie wieder öfter verwendet werden. Es entstanden moderne funktionale und logische Sprachen wie:
- *Erlang:* logische Programmiersprache; inspiriert von Prolog
- *Clojure:* funktionale Programmiersprache; "Dialekt" von LISP

Desweiteren entstanden auch *Multiparadigmensprachen*, diese haben neben funktionalen auch objektorientierte und imperative Aspekte. 
Zu diesen gehören:
- *Ruby*
- *Python* 
- *Scala*
- Apple's *Swift*
- Google's *Go*