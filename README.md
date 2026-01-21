# Übung 11 - Schleifen


## 1. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML1.png" alt="Bildbeschreibung" />
</p>

**Folgende Bedingungen gelten für die Methoden:**
- `printPrim(int start, int ende)`: Gibt alle Primzahlen im Intervall [start, 
ende] aus. Versuchen Sie eine schöne Tabelle zu erstellen – mit maximal 10 Zahlen 
pro Zeile. <br>
**Zusatz:** Sorgen Sie dafür, dass die Einerstellen jeder Zeile untereinanderstehen. 
Gehen Sie von einer maximalen Stellenzahl von 7 Zahlen aus. <br>
**Hinweis:** Verwenden Sie für den Zusatz `System.out.printf`.
- `printEcke1(int hoehe)`: Erzeugt ein rechtwinkeliges Dreieck. Der Parameter 
hoehe bestimmt die Länge der beiden Katheten. <br>
**Beispiel:** `printEcke1(5)`
<p align="center">
  <img src="/assets/images/BSP1.png" alt="Bildbeschreibung" />
</p>

- `printEcke2(int hoehe)`: Erzeugt ein „verkehrtes“ rechtwinkeliges Dreieck. Der 
Parameter hoehe bestimmt die Länge der beiden Katheten. <br>
**Beispiel:** `printEcke2(4)`
<p align="center">
  <img src="/assets/images/BSP2.png" alt="Bildbeschreibung" />
</p>

- `printEcke3(int hoehe, char z1, char z2)`: Erzeugt ein rechtwinkeliges 
Dreieck. Der Parameter hoehe bestimmt die Länge der beiden Katheten, `z1` und `z2`
bestimmen die Zeichen, mit denen das Dreieck dargestellt werden soll. Entlang der 
Katheten sollen `z1` und `z2` abwechselnd ausgegeben werden. <br>
**Beispiel:** `printEcke3(5, '+', '-')`
<p align="center">
  <img src="/assets/images/BSP3.png" alt="Bildbeschreibung" />
</p>

- `printEcke4(int hoehe, char z1, char z2)`: Erzeugt ein rechtwinkeliges 
Dreieck. Der Parameter hoehe bestimmt die Länge der beiden Katheten, `z1` und `z2`
bestimmen die Zeichen, mit denen das Dreieck dargestellt werden soll. Die Seiten 
sollen mit `z1` dargestellt und das Innere des Dreiecks mit `z2` befüllt werden.<br>
**Beispiel:** `printEcke4(5, '+', '-')`
<p align="center">
  <img src="/assets/images/BSP4.png" alt="Bildbeschreibung" />
</p>

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm. Verwenden Sie den Scanner!

## 2. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML2.png" alt="Bildbeschreibung" />
</p>

**Folgende Bedingungen gelten für die Methoden:**
- `drawChars(char ch, int number)`: Zeichnet eine Anzahl von Zeichen. <br>
**Hinweis:** `drawChars(‘\n‘, 1)` erzeugt einen Zeilenvorschub. <br>
**Beispiel:** `drawChars('A', 5)`
<p align="center">
  <img src="/assets/images/BSP5.png" alt="Bildbeschreibung" />
</p>

- `drawRectangle(char ch, int width, int height, int pos)`:  Zeichnet 
ein Rechteck. Verwenden Sie dafür die Methode `drawChars`. Der Parameter `pos`
bezeichnet die Startposition des Rechtecks. <br>
**Beispiel:** `drawRectangle('-', 10, 5, 1)`
<p align="center">
  <img src="/assets/images/BSP6.png" alt="Bildbeschreibung" />
</p>

- `drawFilledRectangle(char ch, char fillChar, int width, int height, int pos)`:  Zeichnet ein gefülltes Rechteck. Verwenden Sie dafür die Methode `drawChars`. <br>
**Beispiel:** `drawFilledRectangle('#', '~', 10, 10, 20)`
<p align="center">
  <img src="/assets/images/BSP7.png" alt="Bildbeschreibung" />
</p>

- `drawTree(int pos, char ch, int height, int charFirstLine)`:  Zeichnet einen Baum mit einer angegebenen Höhe. Verwenden Sie dafür die Methode `drawChars`. <br>
**Beispiel:** `drawTree(1, '~', 10, 3)`
<p align="center">
  <img src="/assets/images/BSP8.png" alt="Bildbeschreibung" />
</p>

- `drawChristmasTree(char chCrown, char chTrunk)`:  Zeichnet einen 
Christbaum. Verwenden Sie dafür die Methoden `drawTree` und 
`drawFilledRectangle`. <br>
**Beispiel:** `drawChristmasTree('>', 'μ')`
<p align="center">
  <img src="/assets/images/BSP9.png" alt="Bildbeschreibung" />
</p>

- `drawZigZag(int height, char ch, boolean endless)`:  Zeichnet eine Zick-Zack-Linie. Der Parameter `endless=true` gibt an, dass die Zick-Zack Linie unendlich weitergezeichnet werden soll. Verwenden Sie dazu die Methode `drawChars`. <br>
**Beispiel:** `drawZigZag(3, 'o', true)`
<p align="center">
  <img src="/assets/images/BSP10.png" alt="Bildbeschreibung" />
</p>

&nbsp;&nbsp;&nbsp;&nbsp;Damit die Kurve beim Endloszeichnen verfolgt werden kann, muss das Programm 
nach jeder Ausgabe verzögert werden. 
&nbsp;&nbsp;&nbsp;&nbsp;Dazu brauchen Sie folgenden Code:
<p align="center">
  <img src="/assets/images/COD1.png" alt="Bildbeschreibung" />
</p>

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm.

## 3. Aufgabe

Schreiben Sie ein Programm, das den Wettlauf zwischen einem Hasen und einer Schildkröte 
simuliert. Anfangs soll der Benutzer den Gewinner tippen. Danach werden die Auswirkungen 
der verschiedenen Aktionen ausgegeben. Um das Geschehen mit dem Auge verfolgen zu 
können, soll das Programm wieder verzögert werden. <br>
Gewonnen hat, wer als Erster 70 Zeichen (‚H‘ oder ‚s‘) geschafft hat. Wenn der Benutzer 
richtig getippt hat, erscheint: Gratuliere, Ihr Tipp war richtig! Ansonsten: Leider verloren, 
versuchen Sie es noch einmal! Der Benutzer soll nach jedem Spiel gefragt werden, ob er noch 
einmal spielen soll oder nicht. 


Für die Wahrscheinlichkeiten sollen folgende Zufallszahlen verwendet werden:

<div align="center">

| Tier | Aktion | Wahrscheinlichkeit | Positionsänderung |
|:----------:|:----------:|:----------:|:----------:|
| Hase  | schläft     | 20%     | 0     |
| Hase  | großer Sprung     | 20%     | +9     |
| Hase  | großer Rutscher     | 10%     | -12     |
| Hase  | kleiner Sprung     | 30%     | +1     |
| Hase  | kleiner Rutscher     | 20%     | -2     |
| Schildkröte  | großer Schritt     | 50%     | +3     |
| Schildkröte  | Rutscher     | 20%     | -6     |
| Schildkröte  | kleiner Schritt     | 30%     | +1     |

</div>

Beispielhafte Ausgabe:
<p align="center">
  <img src="/assets/images/AUS1.png" alt="Bildbeschreibung" />
</p>

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm. Verwenden Sie den Scanner!
