# Java Cheat Sheet

- [Java Cheat Sheet](#java-cheat-sheet)
  - [Operatoren](#operatoren)
  - [Input & Output](#input--output)
    - [Text Ausgabe auf der Komandoziele](#text-ausgabe-auf-der-komandoziele)
    - [Einlesen eines Strings von der Komandozeile](#einlesen-eines-strings-von-der-komandozeile)
      - [Einen Scanner benutzen](#einen-scanner-benutzen)
      - [Mit InputStreamReader](#mit-inputstreamreader)
    - [Einlesen einer Datei](#einlesen-einer-datei)
    - [Einlesen einer Webseite](#einlesen-einer-webseite)
    - [Datentypen](#datentypen)
      - [Numerisch](#numerisch)
  - [Schleifen und das switch-Statement](#schleifen-und-das-switch-statement)
    - [Switch-Statement](#switch-statement)
  - [Listen und Arrays](#listen-und-arrays)
  - [Keywords](#keywords)
  - [Vererbung](#vererbung)

## Operatoren

```java
+   // Addition or concatenation fo strings
-   // Subtraction
*   // Multiplikation
/   // Division
%   // Modulo         "Rest einer Division"

++a // Pre increment  "erst erhöhen dann verwenden"
--a // Pre decrement   erst verringern dann verwenden"

a++ // Post increment "erst verwenden dann erhöhen"
a-- // Post decrement "erst verwenden dann verringern"

==  // Logical EQUALS "A entspricht B"
!   // Logical NOT    "Umgekehrter Zustand"
!=  // NOT EQUAL      "A entspricht nicht B"
&&  // Logical AND    "A und B"
||  // Logical OR     "A oder B oder beide"
^   // Logical XOR    "A oder B aber nicht beides"

&   // bitwiese AND
|   // bitwiese OR
^   // bitwiese XOR
```

## Input & Output

### Text Ausgabe auf der Komandoziele

```java
System.out.println("Hallo  Welt!");
```

### Einlesen eines Strings von der Komandozeile

#### Einen Scanner benutzen

```java
import java.util.Scanner;
...
// The Scanner needs an input Stream, here System.in
Scanner reader = new Scanner(System.in);
String input = reader.readLine();
```

#### Mit InputStreamReader

```java
import java.io.*;
...
// get the keyboard input stream
InputStreamReader isr = new InputStreamReader(System.in);
BufferedReader keyboard = new BufferedReader(isr);
String input = keyboard.readLine();
```

### Einlesen einer Datei

```java
import java.io.*;
...
File file = new File(file1);
FileInputStream fins = new FileInputStream(file);   // creating the inputstream
InputStreamReader isr = new InputStreamReader(fins); // creating a stream reader
BufferedReader fileinput = new BufferedReader(isr);  // needed for reading whole lines

String line = fileinput.readLine();S
fileinput.close() // if not needed anymore
```

### Einlesen einer Webseite

```java
import java.io.*;
import java.net.*;
...
URL url = new URL("https://www.tenouk.com/cplusstandard.html");
FilterInputStream fis = (FilterInputStream) url.openStream();
InputStreamReader netisr = new InputStreamReader(fis);
BufferedReader page = new BufferedReader(netisr);
String line = page.readLine(); //! returns null if the end is reached

while (line != null) {
    System.out.println(line);
    line = target.readLine();
}
```

### Datentypen

#### Numerisch

```java
byte  b = (byte) 0;
short s = (short) 1
int   i = 2;
long  l = 3;
BigInteger bi = new BigInteger("6");

float f  = 0.4;
double d = 0.5;
BigDecimal bi = new BigDecimal("0.7");
```

## Schleifen und das switch-Statement

### Switch-Statement

- x müssen Konstanten oder Literale primitiver Datentypen sein (`byte, short, char, int, String`)

```java
switch (x) {
  case value1: statement1;
        break;
  case value2: statement2;
        break;
        ...
  case valuen: statementn;
        break;
  default: statement;
        break;
}
```

## Listen und Arrays

```java
import java.util.ArrayList;
import java.util.ListIterator;

/**
 * ListIter
 */
public class ListIter {

public static void main(String[] args) {

      ArrayList a = new ArrayList();

      a.add(new Integer(1));
      a.add(new Integer(2));
      a.add(new Integer(3));

      ListIterator it = a.listIterator(); // ListIterator
      // Eine ArrayList durchlaufen
      while (it.hasNext()) {
            System.out.println(it.next());
      }

      ArrayList<Long> l = new ArrayList<Long>();

      l.add(new Long(23));
      l.add(new Long(24));
      l.add(new Long(25));

      for (Long o : l) { // Automatischer ListIterator
            System.out.println(o);
      }

      // primitve Arrays
      int[] iarr = new int[3];
      iarr[0] = 0;
      iarr[1] = 1;
      iarr[2] = 2;
      System.out.println("iarr.length " + iarr.length); // 3

      for (int i : iarr) {
            System.out.println(i);
      }

      double[][] darr = new double[2][2];
      darr[0][0] = 1.1;
      darr[0][1] = 1.2;
      darr[1][0] = 2.1;
      darr[1][1] = 2.2;
      System.out.println("darr.length " + darr.length); // 2

      for (double[] ds : darr) {
            for (double ds2 : ds) {
                  System.out.print(ds2 + " ");
            }
            System.out.println();
      }


      int[][] zeilenVektor = { { 1, 2, 3 } };
      for (int[] is : zeilenVektor) {
            for (int is2 : is) {
                  System.out.print(is2 + " ");
            }
            System.out.println();
      }

      int[][] spaltenVektor = { { 1 }, { 2 }, { 3 } };
      for (int[] is : spaltenVektor) {
            for (int is2 : is) {
                  System.out.print(is2 + " ");
            }
            System.out.println();
      }
      Wochentag d = Wochentag.Dienstag;
      System.out.println(d);
}
      enum Wochentag { Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag};
}
```

## Keywords

- **final:** entspricht einer Konstante ist nicht mehr veränderbar
- **static:** bedeutet, das eine Variable oder eine Methode die mit `public` gekennzeichnet ist unhabhängig von einem Objekt aufgerufen und verwendet werden kann.
- **private:** bedeutet, das man nur von innerhalb der Klasse auf die mit `private` gekennzeichneten Methoden und Variablen zugreifen kann.

## Vererbung 

- **extends** sorgt dafür das `BetterBR` alles Methoden und Instanzvariablen die in `BufferedReader` definiert wurden auch besitzt. (sie werden quasi vereerbt...)

```java
class BetterBR extends BufferedReader{
...
}
```

