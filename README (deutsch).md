# SparkBlitzSyntax
###### © by [Spark Fountain](http://sparkfountain.de/), 2013 - 2015

*Bitte beachte, dass dieses Dokument noch sehr unvollständig ist und kontinuierlich aktualisiert wird.*

## Herangehensweise
Bei **BlitzBasic** handelt es sich - was eindeutig am Namen erkennbar ist - um einen speziellen Dialekt
der Programmiersprache **BASIC** (englisch *B*eginner’s *A*ll-purpose *S*ymbolic *I*nstruction *C*ode).
Diese anfängerfreundliche Sprache zeichnet sich durch einige Merkmale aus. Bedeutend sind unter anderem
die häufig verwendeten "Einzeiler", also Befehle, die lediglich eine Codezeile zur Deklarierung benötigen.
In anderen Sprachen wie **Java**, **C** oder **JavaScript** gibt es hingegen Konstrukte, die über viele
Zeilen hinweg gehen - man denke etwa an Klassen- oder Methodendefinitionen, an deren Beginn und Ende sich
zahlreiche Klammern versammeln und leicht für Unübersichtlichkeit sorgen können. In BASIC gibt stattdessen
für umfangreichere Codeblöcke meist Kommandos, die den Beginn einleiten und durch das Schlüsselwort **End**
vor dem gleichen Kommandonamen wieder abgeschlossen werden. Ein bekanntes Beispiel dafür sind 
**If-Else-Endif**-Anweisungen.

Früher wurde auch häufig der Befehl `GOTO` eingesetzt, um an bestimmte Codeabschnitte zu springen. Das
kann schnell zum sogenannten "Spaghetticode" führen und sollte darum in BlitzBasic grundsätzlich vermieden
werden. Zudem ist BlitzBasic ja viel moderner und kennt Funktionen, die man bei Bedarf aufrufen kann.

Die Regeln der *SparkBlitzSyntax* bieten einen Vorschlag, die leichte Lesbarkeit von (Blitz)Basic-Code
mit der gängigen Syntax moderner und häufig verwendeter Programmiersprachen zu kombinieren. Dabei werden
vor allem drei Prinzipien verfolgt, wie der Quellcode sein soll:

#### 1. Sauber und intuitiv
BlitzBasic bietet viele Möglichkeiten, gültigen Code ohne strikte Regeln zu schreiben. So wird Groß- und
Kleinschreibung bei Funktions- und Variablennamen ignoriert, auf viele Befehle folgen die Parameter per
einfacher Auflistung (ohne Klammern um den Funktionsnamen) und lokale Variablen müssen nie initialisiert
werden, sondern können einfach irgendwo angelegt und verwendet werden, wie man sie gerade braucht. Das
sorgt bei Anfängern oft für Erleichterung, kann einen erfahrenen Programmierer aber auch mal zur Weißglut
treiben - weil es gelegentlich sogar zu Verwirrungen führt. Aus diesen Gründen legt die SparkBlitzSyntax
überall eindeutige Code-Schreibregeln fest, wo der BlitzBasic-Compiler sonst sehr liberal ist. Die jeweils
verwendete Syntaxform ähnelt dabei den "etablierten" Programmiersprachen und ist insbesondere für 
Fortgeschritte sehr intuitiv nachvollziehbar.

#### 2. Eindeutig statt variabel
Wie bereits erwähnt, lässt sich mit Variablen bei BlitzBasic viel herumschludern. Auch die Reihenfolge, in
der Funktionen, Typen, Includes und andere Sachen im Code geschrieben werden dürfen, ist nahezu beliebig.
Die SparkBlitzSyntax gibt eine eindeutige Reihenfolge für verschiedene Elemente des Quellcodes vor und
verlangt, dass Variablen stets vor dem ersten Benutzen deklariert werden und der zugeordnete Datentyp bei
jeder Verwendung eindeutig gekennzeichnet ist (z.B. das `$`-Zeichen als Suffix bei Strings).

#### 3. Mächtig und flexibel
Leider bringt BlitzBasic von Hause aus nicht viele modulare und objektorientierte Konstrukte mit sich.
Mithilfe der SparkBlitzSyntax soll versucht werden, trotz der Beschränkungen die Möglichkeiten voll
auszuschöpfen und explizit zu zeigen, mit welchen Tricks man aus BlitzBasic noch das ein oder andere
herausholen kann. Es werden Methoden erläutert, um flexible Datentypen zu realisieren, neue Datentypen zu
erstellen und verwenden (z.B. Collections) oder Funktionen zu überschreiben und mehrere Variablen als
Rückgabewerte zu haben.


## Grundlagen
Hier findest du eine Übersicht der Regeln, welche tagtäglich beim Schreiben von großen und kleinen Programmen
relevant sind.

- *Variablennamen beginnen mit Kleinbuchstaben.*
Jede Variable muss mit einem kleinen Buchstaben aus dem Alphabet beginnen - nicht etwa mit Sonderzeichen.

- *Konstantennamen bestehen nur aus Großbuchstaben.*
Jede Konstante hat einen Namen, der nur aus Großbuchstaben besteht. Sonderzeichen sind erlaubt, sofern sie nicht
direkt am Anfang stehen.

- *Funktionsnamen beginnen mit Großbuchstaben.*
Funktionen und Befehle bilden nach der SparkBlitzSyntax eine gewisse Einheit.

- *Namen, die aus mehreren Wörtern bestehen, sollten als solche erkennbar sein.*
Oft kann es hilfreich sein, einer Variable oder Funktionen einen etwas längeren Namen zu geben, der erklärt,
was dort deklariert bzw. ausgeführt wird. Die einzelnen Wörter, aus denen die Bezeichnernamen bestehen, sollen
leicht erkennbar sein. Deshalb beginnt jedes Teilwort in Funktions- und Variablennamen mit einen Großbuchstaben,
sofern es sich nicht um das erste Teilwort handelt. Zwei kurze Beispiele: Eine Funktion zum Bewegen der 
Spielfigur kann heißen `



## Ästhetik
Unter dieser Rubrik befinden sich alle Regeln, die auch so manchem Fremdcode-Leser entgegen kommen.

- *Coding Language = English*
Mehrsprachigkeit in manchen Anwendungen und Spielen erwünscht, aber im Quellcode stört die Verwendung mehrerer
natürlicher Sprachen meistens. Variablen, Funktionen und Kommentare sollten auf Englisch geschrieben werden,
um einen leichteren Lesefluss zu ermöglichen. Außerdem sollte jeder, der sich deinem Code mit den Augen nähert,
schon ein paar Englischkenntnisse haben und nicht den Knall kriegen, wenn außer englischen Codebefehlen
haufenweise fremdsprachiges Zeug drin steht.
