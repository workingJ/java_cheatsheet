# Java Code Cheet

- [Java Code Cheet](#java-code-cheet)
  - [**Kommentare** in Java](#kommentare-in-java)
  - [**primitive** Datentypen](#primitive-datentypen)
  - [**komplexe** Datentypen](#komplexe-datentypen)
    - [**Strings**](#strings)
    - [**Arrays**](#arrays)
    - [**Listen**](#listen)
    - [**Enumeration**](#enumeration)
  - [Operatoren](#operatoren)
  - [Schleifen](#schleifen)
    - [**while** Schleifen](#while-schleifen)
    - [**for** Schleifen](#for-schleifen)
    - [**break** Statement](#break-statement)
    - [**do-while** Schleife](#do-while-schleife)
  - [Verzweigungen](#verzweigungen)
    - [**if** Anweisung](#if-anweisung)
    - [**switch** Anweisung](#switch-anweisung)
  - [Eingaben](#eingaben)
    - [Einlesen von Komandozeile mit einem Scanner**](#einlesen-von-komandozeile-mit-einem-scanner)
    - [**Mit InputStreamReader**](#mit-inputstreamreader)
    - [**Einlesen einer Datei**](#einlesen-einer-datei)
    - [**Einlesen einer Webseite**](#einlesen-einer-webseite)
  - [Ausgaben](#ausgaben)
    - [Printing](#printing)

## **Kommentare** in Java

- Vor jeder Zeile, die mit dem Wort class beginnt, sollte ein Kommentar stehen, der die Klasse beschreibt.
- Kommentare sollten dazu dienen, Dinge zu erklären, die nicht unmittelbar aus dem Code abgelesen werden können.
- Das Warum beschreiben und nicht das Wie
- Kommentare sollten nicht in der Mitte von einem Statement auftauchen.

```java
// Dies ist ein einzeiliger Kommentar

/* Dieser Kommentar ist mehrzeilig
Dieser Kommentar ist mehrzeilig
Dieser Kommentar ist mehrzeilig
Dieser Kommentar ist mehrzeilig
*/

/// Dies ist ein Dokumentations-Kommentar (Doc-Comment)

/** Dies ist ei  Doc-Comment
 * Geschwindigkeit ist verantwortlich für die Umrechnung
 * verschiedener Geschwindigkeitsmasse untereinander.
 *
 * @author Dein Ponny
 * @version 1.0
 * ...
 */
```

## **primitive** Datentypen

```java
byte myByte = 127;        // 2⁸   -128 - 127
short myShort = 255;      // 2¹⁶  -32768 - 32767
int myInt = 444;          // 2³²  -2147483648 - 2147483647
long myLong = 88888;      // 2⁶⁴  -9223372036854775808 - 9223372036854775807

float myFloat = 234F;     // 1.4E-45 - 3.4028235E38
double myDouble = 7.3426; // 4.9E-324 - 1.7976931348623157E308

boolean myBool = true;    // true
boolean myBool = 5 > 8;   // false

char myChar = 'a';
```

## **komplexe** Datentypen

```java
BigInteger bi = new BigInteger("6");
BigDecimal bi = new BigDecimal("0.7");
```

### **Strings**

Eine Klasse und kein primitiver Datentyp. Ein Variable vom Type String ist eine Referenz auf ein String-Objekt.

```java
String text1 = "Name"; // Referenz (Pionter) auf ein String-Objekt
String text2 = null;   // Null-Pointer ("leerer String")
String text3 = text1 + " " + text2; //"Name Joe"
```

### **Arrays**

```java
// primitve Arrays anlegen und initialisieren
int[] values1;
values1 = new int[3];
double[] values2 = {1.6, 2.5, 3.4};

int[] iarr = new int[3];
iarr[0] = 0;
iarr[1] = 1;
iarr[2] = 2;
System.out.println("iarr.length " + iarr.length); // 3

// Array Itterieren
for (int i : iarr) {
    System.out.println(i);
}

String[] words = new String[3];
words[0] = "Hallo";
words[1] = "neue";
words[2] = "Welt";

// Array Itterieren
for (int i = 0; i < values2.length; i++) {
    System.out.println(values2[i]);
}

// Itterieren mit foreach
for (String word : words) {
    System.out.println(word);
}

// mehr Dimensionale Arrays anlegen und initialisieren
double[][] darr = new double[2][2];

darr[0][0] = 1.1;
darr[0][1] = 1.2;
darr[1][0] = 2.1;
darr[1][1] = 2.2;
// Arraylänge ausgeben
System.out.println("Arraylänge: " + darr.length); // 2

// itterieren
for (double[] ds : darr) {
    for (double ds2 : ds) {
            System.out.print(ds2 + " ");
    }
    System.out.println();
}

// zeilenVector nitialisieren
int[][] zeilenVektor = { { 1, 2, 3 } };

// zeilenVector itterieten
for (int[] is : zeilenVektor) {
    for (int is2 : is) {
        System.out.print(is2 + " ");
    }
    System.out.println();
}

// spaltenVector initialisieren
int[][] spaltenVektor = { { 1 }, { 2 }, { 3 } };

// zeilenVector itterieten
for (int[] is : spaltenVektor) {
    for (int is2 : is) {
            System.out.print(is2 + " ");
    }
    System.out.println();
}
```

### **Listen**

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
    }
```

### **Enumeration**

```java
    enum Wochentag { Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag};

    Wochentag d = Wochentag.Dienstag;
    System.out.println(d);
```

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

## Schleifen

### **while** Schleifen

```java
while (condition == true) {
    condition++;
}
```

### **for** Schleifen

```java
for (;;) {
    // Endlos Schleifen
}
```

```java
for (int i = 0; i < args.length; i++) {
    ...
}
```

### **break** Statement

```java
while(contidion) {
    if(condition > 2) break;
    condition++;
}
```

### **do-while** Schleife

```java
byte i = 0;
do {
    i++;
}
while(i < 10);
```

## Verzweigungen

### **if** Anweisung

```java
if (condition) {
    ...
}
```

```java
if (condition) {
    ...
} else {

}
```

```java
if (condition) {
    ...
} else if (condition) {
    ...
} else if (condition) {
    ...
} else {
    ...
}
```

### **switch** Anweisung

Argumente fpr switch müssen Konstanten oder Literale primitiver Datentypen sein (`byte, short, char, int, String`)

```java
switch (argument) {
    case value:

        break;
    case value:

        break;
    default:
        break;
}
```

## Eingaben

### Einlesen von Komandozeile mit einem [Scanner](https://docs.oracle.com/javase/8/docs/api/java/util/Scanner.html)**

```java
import java.util.Scanner;
...
// The Scanner needs an input Stream, here System.in
Scanner input = new Scanner(System.in);
String line = input.nextLine();
int intv = input.nextInt();
double doublev = input.nextDouble();
```

### **Mit InputStreamReader**

```java
import java.io.*;
...
// get the keyboard input stream
InputStreamReader isr = new InputStreamReader(System.in);
BufferedReader keyboard = new BufferedReader(isr);
String input = keyboard.readLine();
```

### **Einlesen einer Datei**

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

### **Einlesen einer Webseite**

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

## Ausgaben

### Printing

```java
System.out.print(Object);
System.out.println("Hallo Welt");
System.out.printf("Ausgabe: %d", 10);
```
