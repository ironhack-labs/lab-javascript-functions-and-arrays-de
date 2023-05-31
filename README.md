
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | JS Funktionen & Arrays

<br>   
## Einführung  

Das Manipulieren von Arrays in Code ist eine sehr häufige Operation. Egal, ob Du eine Gesamtsumme für einen Einkaufswagen erstellst, nur die Vornamen aus einer Liste von Personen herausgreifst oder ein Stück auf einem Schachbrett bewegst, Du wirst wahrscheinlich auf irgendeine Weise ein Array modifizieren oder manipulieren.

## Einrichtung

- Fork dieses Repositories
- Klone es auf Deinem Rechner



## Abgabe

- Führe nach Abschluss des Labors die folgenden Befehle aus:

```bash 
git add .
git commit -m "Solved lab"
git push origin master
```   
- Erstelle eine Pull-Request, damit Deine TAs Deine Arbeit überprüfen können.

<br>   


## Anweisungen


Du wirst an der Datei `src/functions-and-arrays.js` arbeiten, die bereits in der Datei `index.html` geladen ist.

Um den JavaScript-Code auszuführen, öffne die Datei `index.html` und verwende die [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)-Erweiterung von VSCode.


Um die Ausgabe deines JavaScript-Codes zu sehen, öffne die [Konsole in den Entwicklertools](https://developer.chrome.com/docs/devtools/open/#console).

Achte beim Befolgen der Anweisungen für jede Iteration darauf, die Anweisungen sorgfältig zu lesen, um die Aufgabenanforderungen vollständig zu verstehen. Beeile Dich nicht. Nimm Dir Zeit, um jede Iteration sorgfältig zu lesen.


### Hinweis zu Tests

Dieses LAB, sowie einige andere LABs, an denen du während des Bootcamps arbeiten wirst, sind mit Unit-Tests ausgestattet, um automatisiertes Feedback zu deinem Fortschritt zu geben.

**Nachdem du die grundlegenden Iterationen abgeschlossen hast**, gehe zum Abschnitt **"Teste deinen Code"** unten. Dort wirst du aufgefordert, die Testabhängigkeiten zu installieren und die Tests auszuführen, um zu überprüfen, wie viele Tests dein Code besteht.



<br>   

### Iteration #1: Finde das Maximum

Implementiere die Funktion `maxOfTwoNumbers`, die zwei Zahlen als Argumente entgegennimmt und die größte zurückgibt.

<br>   

### Iteration #2: Finde das längste Wort

Implementiere die Funktion `findLongestWord`, die als Argument ein Array von Wörtern annimmt und das längste Wort zurückgibt. Wenn es zwei mit der gleichen Länge gibt, sollte das erste Vorkommen zurückgegeben werden.

Du kannst das folgende Array verwenden, um Deine Lösung zu testen:

```javascript 
const words = ['mystery', 'brother', 'aviator', 'crocodile', 'pearl', 'orchard', 'crackpot']; 
```   
<br>   

### Iteration #3: Die Summe berechnen

Eine Summe zu berechnen kann so einfach sein wie eine Schleife über ein Array zu iterieren und jedes der Elemente zusammen zu addieren.

Implementiere die Funktion mit dem Namen `sumNumbers`, die ein Array von Zahlen als Argument nimmt und die Summe aller Zahlen im Array zurückgibt. Später im Kurs werden wir lernen, wie man dies mithilfe der `reduce`-Methode des Arrays machen kann, was die Arbeit erheblich erleichtert. Für jetzt wollen wir die _"deklarative"_ Art und Weise üben, Werte hinzuzufügen, indem wir Schleifen verwenden.

Du kannst das folgende Array verwenden, um deine Lösung zu testen:

```javascript 
const numbers = [6, 12, 1, 18, 13, 16, 2, 1, 8, 10]; 
```   
<br>   

#### Bonus - Iteration #3.1: Eine generische `sum()` Funktion

**Ziel: Lerne, wie man den Code refaktorisiert.** :muscle:

In der Iteration 3 hast Du eine Funktion erstellt, die die Summe eines Arrays von Zahlen zurückgibt. Aber was ist, wenn wir wissen wollten, wie viel die Summe der Längen aller Wörter in einem Array beträgt? Was ist, wenn wir boolesche Werte dazumischen wollen? Wir könnten die obige Funktion nicht verwenden, oder besser gesagt, wir müssten sie ein wenig anpassen, damit sie wiederverwendet werden kann, unabhängig von dem, was im Array steht, das als Argument übergeben wird, wenn die Funktion `sumNumbers()` aufgerufen wird.

Hier wenden wir ein Konzept an, das wir **Polymorphismus** nennen, das heißt, die Verarbeitung der Eingabe von Funktionen unabhängig von den Typen, die übergeben werden.

Implementieren wir die Funktion `sum()`, die die Summe für ein Array mit (_fast_) jedem Datentyp berechnet. Beachte, dass Strings ihre Länge zur Summe beitragen sollten, und boolesche Werte sollten in ihre entsprechenden numerischen Werte umgewandelt werden. Überprüfe die Tests für weitere Details.

Du kannst das folgende Array verwenden, um Deine Lösung zu testen:

```javascript 
const mixedArr = [6, 12, 'miami', 1, true, 'barca', '200', 'lisboa', 8, 10];    
 // should return: 57 
 ```   
<br>   

### Iteration #4: Durchschnitt berechnen

Das Berechnen eines Durchschnitts ist eine sehr häufige Aufgabe. Lass uns ein bisschen üben.

**Die Logik dahinter:**

1. Finde die Summe wie wir es in der ersten Übung gemacht haben (oder wie wäre es mit dem Wiederverwenden von _sumNumbers()_?)
2. Nimm diese Summe und teile sie durch die Anzahl der Elemente in der Liste.

<br>   

#### Level 1: Array von Zahlen

Implementiere die Funktion `averageNumbers`, die ein Array von Zahlen erwartet und den Durchschnitt der Zahlen zurückgibt:

Du kannst das folgende Array verwenden, um Deine Lösung zu testen:

```javascript 
const numbers = [2, 6, 9, 10, 7, 4, 1, 9]; 
```   
<br>   

#### Level 2: Array of strings

Implementiere die Funktion averageWordLength, die ein Array von Wörtern als einzigen Argument erwartet und die durchschnittliche Länge der Wörter zurückgibt:

Du kannst das folgende Array verwenden, um deine Lösung zu testen:

```javascript 
const words = ['seat', 'correspond', 'linen', 'motif', 'hole', 'smell', 'smart', 'chaos', 'fuel', 'palace']; 
```   
<br>   

#### Bonus - Iteration #4.1: Eine generische Funktion 'avg()'

Erstelle die Funktion `avg(arr)`, die ein gemischtes Array als Argument annimmt und den Durchschnitt berechnet. Als gemischtes Array gelten Arrays, die mit Zahlen, Strings und/oder Booleans gefüllt sind.

Die nicht-numerischen Werte sollten wie folgt gezählt werden:

- Booleans: 'true' zählt als '1' und 'false' zählt als '0'.
- Strings: Verwende die Länge des Strings als numerischen Wert.


```javascript 
const mixedArr = [6, 12, 'miami', 1, true, 'barca', '200', 'lisboa', 8, 10];    
 // should return: 5.7
  ```   
<br>   

### Iteration #5: Eindeutige Arrays

Nimm das folgende Array, entferne die Duplikate und gib ein neues Array zurück. Du wirst wahrscheinlich die Array-Methode [`indexOf`] ([https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)) verwenden wollen.

Mache dies in Form einer Funktion `uniquifyArray`, die ein Array von Wörtern als Argument erhält.

Du kannst das folgende Array verwenden, um deine Lösung zu testen:

```javascript 
const words = [    
'crab', 'poison', 'contagious', 'simple', 'bring', 'sharp', 'playground', 'poison', 'communion', 'simple', 'bring']; 
```   
<br>   

### Iteration #6: Elemente finden

Lass uns eine einfache Array-Suche erstellen.

Erstelle eine Funktion namens `doesWordExist`, die ein Array von Wörtern als ein Argument und ein zu suchendes Wort als das andere Argument entgegennimmt. Gib `true` zurück, wenn es existiert, ansonsten gib `false` zurück. Verwende für diese Aufgabe nicht `indexOf`.

Du kannst das folgende Array verwenden, um deine Lösung zu testen:

```javascript 
const words = ['machine', 'subset', 'trouble', 'starting', 'matter', 'eating', 'truth', 'disobedience']; 
```   
<br>   

### Iteration #7: Wiederholungszählung

Erstelle eine Funktion namens `howManyTimes`, die als erstes Argument ein Array von Wörtern und als zweites Argument ein Wort, nach dem gesucht werden soll, erhält. Die Funktion gibt die Anzahl der Male zurück, in denen das Wort im Array vorkommt.

Du kannst das folgende Array verwenden, um deine Lösung zu testen:

```javascript 
const words = [    
'machine', 'matter', 'subset', 'trouble', 'starting', 'matter', 'eating', 'matter', 'truth', 'disobedience', 'matter']; 
```   
<br>   

### Bonus - Iteration #8: Produkt von benachbarten Zahlen

Was ist das größte Produkt von vier benachbarten Zahlen? Wir betrachten als benachbart vier Zahlen, die horizontal oder vertikal nebeneinander stehen.

Zum Beispiel, wenn wir eine 5x5 Matrix haben:

```bash 
[ 1,  2, 3, 4, 5] [ 1, 20, 3, 4, 5] [ 1, 20, 3, 4, 5] [ 1, 20, 3, 4, 5] [ 1,  4, 3, 4, 5] 
```   

Das größte Produkt wäre `20`x`20`x`20`x`4` = `32000`.

Erstelle die Funktion `greatestProduct(matrix)`, um es in der 20x20-Matrix unten zu finden!

```javascript 
const matrix = [    
[08, 02, 22, 97, 38, 15, 00, 40, 00, 75, 04, 05, 07, 78, 52, 12, 50, 77, 91, 08], [49, 49, 99, 40, 17, 81, 18, 57, 60, 87, 17, 40, 98, 43, 69, 48, 04, 56, 62, 00], [81, 49, 31, 73, 55, 79, 14, 29, 93, 71, 40, 67, 53, 88, 30, 03, 49, 13, 36, 65], [52, 70, 95, 23, 04, 60, 11, 42, 69, 24, 68, 56, 01, 32, 56, 71, 37, 02, 36, 91], [22, 31, 16, 71, 51, 67, 63, 89, 41, 92, 36, 54, 22, 40, 40, 28, 66, 33, 13, 80], [24, 47, 32, 60, 99, 03, 45, 02, 44, 75, 33, 53, 78, 36, 84, 20, 35, 17, 12, 50], [32, 98, 81, 28, 64, 23, 67, 10, 26, 38, 40, 67, 59, 54, 70, 66, 18, 38, 64, 70], [67, 26, 20, 68, 02, 62, 12, 20, 95, 63, 94, 39, 63, 08, 40, 91, 66, 49, 94, 21], [24, 55, 58, 05, 66, 73, 99, 26, 97, 17, 78, 78, 96, 83, 14, 88, 34, 89, 63, 72], [21, 36, 23, 09, 75, 00, 76, 44, 20, 45, 35, 14, 00, 61, 33, 97, 34, 31, 33, 95], [78, 17, 53, 28, 22, 75, 31, 67, 15, 94, 03, 80, 04, 62, 16, 14, 09, 53, 56, 92], [16, 39, 05, 42, 96, 35, 31, 47, 55, 58, 88, 24, 00, 17, 54, 24, 36, 29, 85, 57], [86, 56, 00, 48, 35, 71, 89, 07, 05, 44, 44, 37, 44, 60, 21, 58, 51, 54, 17, 58], [19, 80, 81, 68, 05, 94, 47, 69, 28, 73, 92, 13, 86, 52, 17, 77, 04, 89, 55, 40], [04, 52, 08, 83, 97, 35, 99, 16, 07, 97, 57, 32, 16, 26, 26, 79, 33, 27, 98, 66], [88, 36, 68, 87, 57, 62, 20, 72, 03, 46, 33, 67, 46, 55, 12, 32, 63, 93, 53, 69], [04, 42, 16, 73, 38, 25, 39, 11, 24, 94, 72, 18, 08, 46, 29, 32, 40, 62, 76, 36], [20, 69, 36, 41, 72, 30, 23, 88, 34, 62, 99, 69, 82, 67, 59, 85, 74, 04, 36, 16], [20, 73, 35, 29, 78, 31, 90, 01, 74, 31, 49, 71, 48, 86, 81, 16, 23, 57, 05, 54], [01, 70, 54, 71, 83, 51, 54, 69, 16, 92, 33, 48, 61, 43, 52, 01, 89, 19, 67, 48]]; 
```   
<br>   

### Bonus - Iteration #8.1: Produkt von Diagonalen

Folge der Logik, die du in Iteration #8 verwendet hast, und deklariere eine Funktion namens `greatestProductOfDiagonals(matrix)`. Sie nimmt eine Matrix als Parameter entgegen und gibt das größte Produkt von vier Werten zurück, die diagonal in beide Richtungen angeordnet sind.

<br>   



## Teste deinen Code

<br>  

### Automatisierte Tests

Automatisiertes Software-Testing ist der Prozess des automatisierten Testens einer Anwendung, um zu überprüfen, ob sie den technischen Anforderungen entspricht und sich wie erwartet verhält.

Eine gute Testabdeckung kann dir ein beruhigendes Gefühl geben, da du sicher sein kannst, dass du Verbesserungen an deiner Arbeit vornehmen kannst, während du weißt, dass du keine bereits entwickelte Funktionen beeinträchtigst.



<br>   

### Testing mit Jest

Jest ist ein automatisierter Test-Runner für JavaScript.

Um deine Tests auszuführen, öffne dein Terminal im Stammverzeichnis des Labs, führe `npm install` aus, um deine Abhängigkeiten zu installieren, und führe `npm run test:watch` aus, um die Tests auszuführen und die Datei `lab-solution.html` zu generieren.

```shell 
$ cd lab-javascript-functions-and-arrays
$ npm install
$ npm run test:watch  
```    
 <br>    
 Wenn du die Tests überprüfen möchtest, findest du sie in der Datei `tests/functions-and-arrays.spec.js`.  

Öffne die Datei `lab-solution.html` mithilfe der VSCode-Erweiterung [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

<br>    

#### Bestehe die Tests

Beim Coden mit Tests ist es sehr wichtig, dass Du die Fehlermeldungen sorgfältig liest und verstehst, damit Du genau weißt, was von Deinem Code erwartet wird.

Beachte, dass **Du die Funktionen nicht selbst ausführen musst**, die Tests sind dafür verantwortlich. Du solltest sie nur deklarieren, sicherstellen, dass sie mit den übergebenen Parametern umgehen können und dass sie das zurückgeben, was in den Iterationen und in den Testnachrichten angegeben ist. Für einige Iterationen stellen wir Dir ein Beispiel-Array zur Verfügung, damit Du manuell testen kannst, wenn Du möchtest.

<br>    

**Viel Spaß beim Coden!** :heart: