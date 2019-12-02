# **Heinz Cheat Sheet**

- [**Heinz Cheat Sheet**](#heinz-cheat-sheet)
  - [**Was ist Informatik?**](#was-ist-informatik)
    - [Aspekte der Informatik?](#aspekte-der-informatik)
    - [Was ist ein Computer?](#was-ist-ein-computer)
    - [Was ist eigentlich ein Programm](#was-ist-eigentlich-ein-programm)
  - [**Programmierparadigmen, ein fundamentaler Programmier-Stile**](#programmierparadigmen-ein-fundamentaler-programmier-stile)
    - [Warum Java](#warum-java)
  - [**Java: Ein erster Blick**](#java-ein-erster-blick)
    - [Modelle](#modelle)
    - [Objekte in Java](#objekte-in-java)
    - [Klassen in Java](#klassen-in-java)
    - [Räpresentation in Java](#r%c3%a4presentation-in-java)
    - [Methoden](#methoden)
    - [Nachrichten in Java](#nachrichten-in-java)
      - [Komponenten einer Nachricht](#komponenten-einer-nachricht)
    - [Statements in Java](#statements-in-java)
  - [**Programme**](#programme)
  - [**Keywords**](#keywords)
    - [**`public`:**](#public)
    - [**`private`:**](#private)
    - [**`protected`:**](#protected)
    - [**`static`:**](#static)
    - [**`final`:**](#final)
    - [**`this`:**](#this)
    - [**`extends`:**](#extends)
    - [**`super`:**](#super)
    - [**`exception`**](#exception)
    - [**`abstract`**](#abstract)
  - [**Operatoren**](#operatoren)
  - [**Input & Output**](#input--output)
    - [**Text Ausgabe auf der Komandoziele**](#text-ausgabe-auf-der-komandoziele)
    - [**Einlesen eines Strings von der Komandozeile**](#einlesen-eines-strings-von-der-komandozeile)
      - [**Einen Scanner benutzen**](#einen-scanner-benutzen)
      - [**Mit InputStreamReader**](#mit-inputstreamreader)
    - [**Einlesen einer Datei**](#einlesen-einer-datei)
    - [**Einlesen einer Webseite**](#einlesen-einer-webseite)
    - [**Datentypen**](#datentypen)
      - [**Numerisch**](#numerisch)
  - [**Schleifen und das switch-Statement**](#schleifen-und-das-switch-statement)
    - [**`switch`-Statement**](#switch-statement)
  - [**Listen und Arrays**](#listen-und-arrays)
  - [**Vererbung**](#vererbung)
    - [**`super`-Keyword**](#super-keyword)
    - [**`Protected`-Keyword**](#protected-keyword)
    - [**Overriding**](#overriding)
  - [**Polymorphie**](#polymorphie)
    - [Ausnutzung der Polymorphie](#ausnutzung-der-polymorphie)
    - [Zusammenfassung gemeinsamer Eigenschaften in einer Superklasse](#zusammenfassung-gemeinsamer-eigenschaften-in-einer-superklasse)
    - [Abstrakte Methoden und Klassen (Motivation)](#abstrakte-methoden-und-klassen-motivation)
    - [**`abstract`-Keyword**](#abstract-keyword)
  - [**Interfaces**](#interfaces)
    - [Instanz mehrerer Interfaces](#instanz-mehrerer-interfaces)
    - [Konstanten in Interfaces und Klassen](#konstanten-in-interfaces-und-klassen)
    - [Interfaces ohne Inhalt](#interfaces-ohne-inhalt)
    - [Interface-Implementierung durch anonyme Klasse](#interface-implementierung-durch-anonyme-klasse)
    - [Designentscheidung: Interface oder abstrakte Klasse](#designentscheidung-interface-oder-abstrakte-klasse)
    - [Interface mit Standard-Implementierung](#interface-mit-standard-implementierung)
  - [dynamisches binden](#dynamisches-binden)

## **Was ist Informatik?**

**Informatik lt. Duden:**
Ist die Wissenschaft von der automatischen Verarbeitung von Informationen, besonders der automatischen Verarbeitung mit Hilfe von Digitalrechnern.

**Association of Computing Machinery (ACM):**  
Computer science is the systematic study of algorithms and data structures,
specifically

- their formal properties,
- their mechanical and linguistic realizations, and
- their applications

### Aspekte der Informatik?

- Technische Realisierung
- Effiziente Verfahren
- Theorie
- Programmiersprachen
- Techniken und Tools zur Programmentwicklung

### Was ist ein Computer?

***Ein universell einsetzbares, frei Programmierbares Gerät zur automatischen Datenverarbeitung. Zb. Steuert von Maschinen und Autos, berechnet Messwerte, zum verfassen von Dokumenten etc.***

### Was ist eigentlich ein Programm

- ***Eine Arbeitsvforschrift die so präzise ist das sie von Commputern ausgeführt werden kann.***
- Programme werden in speziellen (formalen) Sprachen, sogenannten ***Programmiersprachen*** formuliert.
- Der Inhalt eines Programmes ist der ***Code***, der von einem Computer ausgeführt wird.

## **[Programmierparadigmen](https://de.wikipedia.org/wiki/Programmierparadigma), ein fundamentaler Programmier-Stile**

- **Imperative Sprachen**: Programm ist Folge von Befehlen, welche Variablenwerte ändern oder den Programmfluss steuern (Pascal, Fortran, C, ...)
- **Funktionale Sprachen**: Programme sind Funktionen mit Parametern, welche wieder Programme sein können (Lisp, Haskell, ...)
- **Logik-basierte Sprachen**: Programm besteht aus Fakten und Regeln, es wird der Beweis einer Aussage gesucht (Prolog, ...)
- **Objektorientierte Sprachen**: Objekte des Anwendungsbereiches können direkt mit ***Eigenschaften*** und ***Verhalten*** modelliert werden, Objekte tauschen ***Nachrichten*** aus, gleiche Objekte werden in ***Klassen*** zusammengefasst (Simula, Smalltalk; Eiffel, C++, Java, ...)

### Warum Java

- Java ist eine **objektorientierte** Sprache mit **imperativem** Kern und **funktionalen** Erweiterungen
- Java ist *die* Sprache des Internet-Zeitalters

## **Java: Ein erster Blick**

### Modelle

Modelle sind (vereinfachende) Darstellungen. Sie enthalten die relevanten Eigenschaften eines modellierten Objektes.
  
- Elemente eines Modells repräsentieren andere, komplexe Dinge.
- Die Elemente eines Modells haben ein bestimmtes, konsistentes Verhalten.
- Die Elemente eines Modells können entsprechend ihrem Verhalten zu verschiedenen Gruppen zusammengefasst werden.
- Externe Aktionen stoßen das Verhalten eines Model an.

### Objekte in Java

Java verwendet für die Elemente eines Modelles ***Objekte***.  

- Alle Objekte des Typs (z.B. Kunde) haben das gleiche Verhalten.  
- In Java wird das *Verhalten eines oder mehrerer Objekte durch ein Programmstück definiert*, welches als ***Klasse*** bezeichnet wird.

### Klassen in Java

- *Kategorien von Elementen eines Modells heißen in Java **Klassen***
- Die *Definition einer Klasse* ist ein *Programmstück (Quell-Code)*, welches spezifiziert, wie sich die  Objekte dieser Klasse verhalten.
- Nachdem eine *Klasse definiert* wurde, *können Objekte* dieser Klasse *erzeugt werden*.
- Jedes Objekt gehört zu genau einer Klasse und wird **Instanz (Exemplar)** dieser Klasse genannt.
- Diese Klassen können verwendet werden, um auf einfache Weise *komplizierte Anwendungen*, z.B. mit *graphischen Benutzeroberflächen* zu realisieren.
- ***Vordefinierte Klassen*** befinden sich in der Standard Bibliothek von Java.

### Räpresentation in Java

Der **Bildschirm (die Konsole)** wird durch ein **vordefiniertes Objekt** repräsentiert.  
Dieses Objekt ist Instanz der Klasse `PrintStream`.
Objekte der Klasse `PrintStream` erlauben das Ausgeben *Zeichenketten*.

```txt
                         -----------------------------
           referenziert |  eine Instanz (ein Objekt)  |  modelliert   ---------
System.out ------------>|     der vordefinierten      |------------->| Monitor |
                        |     Klasse Printstream      |               ---------
                         -----------------------------
```

Eine **Referenz** in Java ist ein Ausdruck, der einen Bezug zu einem **Objekt** herstellt, der das Objekt referenziert.  
`System.out` referenziert ein Objekt der Klasse `PrintStream`, welches den Monitor modelliert.  
`System.out` ist also eine **Referenz auf das `PrintStream`-Objekt**.

### Methoden

- Das in einer Klasse **vordefinierte Verhalten** wird als **Methode** bezeichnet.
- Das aufrufen der Methode eines Objektes entspricht dem Senden der Nachricht an dieses Objekt.

### Nachrichten in Java

Durch Nachrichten aktiviert man das Verhalten eines Objektes, das in Seiner Klasse vordefiniert wurde.  
Schickt man eine **`println`-Nachricht an das Objekt der Klasse `PrintStream`**, wird ein Text auf dem Bildschirm ausgegeben.
Das Verhalten, dass ausgelöst wird, stellt die Klasse `PrintStream` zur Verfügung.
Es handelt sich hierbei um einen **Methoden-Aufruf**.  
Der Code der die Nachricht gesendet (die Methode aufgerufen) hat wird so lange nicht weiter ausgeführt, bis das Verhalten dass die Nachricht ausgelöst hat abgearbeitet ist.

```java
System.out.println("Argument");
```

#### Komponenten einer Nachricht

- **Empfänger**: Die Referenz auf das Empfänger-Objekt zB. `System.out` gefolgt von einem Punkt
- **Methodenselektor**: Der Name des vordefinierten Verhaltens des Objektes zB. `print`, `println`
- **Details**: Die weiteren Informationen die in Klammer eingeschlossen werden zB. `("Argument")`

Hier am Beispiel:

```Java
System.out. // Empfänger, Referenz auf ein Objekt der Klasse print Stream
println("Argument") // Stellt die gesammte Nachricht dar
println()   // Das Verhalten, die vordefinierte Methode
"Argument"  // Details der Nachricht, auch Argument genannt
```

### Statements in Java

- Das Versenden einer Nachricht an ein Objekt ist eine vom Programmierer spezifizierte Aktion.
- Diese Aktion wird vom Computer ausgeführt, wenn das Programm läuft.
- In Java werden alle Aktionen durch Statements spezifiziert.
- der Gesammte Ausdruck `System.out.println("Argument");` ist ein **Statement**

## **Programme**

```java
public class Program1 {
    public static void main (String[ ] arg) {
        System.out.println ("This is my first Java program");
        System.out.println (" but it won't be my last.");
    }
}
```


## **Keywords**


### **`public`:**

 used in a method or variable declaration. It signifies that the method or variable can be accessed by elements residing in other classes.

### **`private`:**

 bedeutet, das man nur von innerhalb der Klasse auf die mit `private` gekennzeichneten Methoden und Variablen zugreifen kann. used in a method or variable declaration. It signifies that the method or variable can only be accessed by other elements of its class.

### **`protected`:**

 used in a method or variable declaration. It signifies that the method or variable can only be accessed by elements residing in its class, subclasses, or classes in the same package.

### **`static`:**

 bedeutet, das eine Variable oder eine Methode die mit `public` gekennzeichnet ist unhabhängig von einem Objekt aufgerufen und verwendet werden kann.

### **`final`:**

 entspricht einer Konstante, wird einmal deklariert und initialisiert und ist danach nicht mehr veränderbar

### **`this`:**

  Repräsentiert eine Instanz der Klasse in der es Auftaucht. z.B. Zugriff auf eine `private` Variable o. eine Methode

### **`extends`:**

 Class X extends class Y to add functionality, either by adding fields or methods to class Y, or by overriding methods of class Y. An interface extends another interface by adding methods. Class X is said to be a subclass of class Y.

### **`super`:**

 used to access members of a class inherited by the class in which it appears. zB. Aufrufen des Konstruktors der übergeorneten Klasse.

### **`exception`**

 An event during program execution that prevents the program from continuing normally; generally, an error. The Java(TM) programming language supports exceptions with the try, catch, and throw keywords. See also exception handler.

### **`abstract`**

 A Java(TM) programming language keyword used in a class definition to specify that a class is not to be instantiated, but rather inherited by other classes. An abstract class can have abstract methods that are not implemented in the abstract class, but in subclasses.
  - **`abstract class`** A class that contains one or more abstract methods, and therefore can never be instantiated. Abstract classes are defined so that other classes can extend them and make them concrete by implementing the abstract methods. Z.b. `class Number` von der alle Wrapper-Klassen der primitiven Datentypen erben.
  - **`abstract method`** A method that has no implementation
- **interface** used to define a collection of method definitions and constant values. It can later be implemented by classes that define this interface with the `implements` keyword.

## **Operatoren**

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

## **Input & Output**

### **Text Ausgabe auf der Komandoziele**

```java
System.out.println("Hallo  Welt!");
```

### **Einlesen eines Strings von der Komandozeile**

#### **Einen Scanner benutzen**

```java
import java.util.Scanner;
...
// The Scanner needs an input Stream, here System.in
Scanner reader = new Scanner(System.in);
String input = reader.readLine();
```

#### **Mit InputStreamReader**

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

### **Datentypen**

#### **Numerisch**

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

## **Schleifen und das switch-Statement**

### **`switch`-Statement**

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

## **Listen und Arrays**

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

## **Vererbung**

Jede Klasse erbt von der `Objekt`-Klasse

- `toString()`, `equals()`, `getClass()`, `hashCode()`, `clone()`

- **extends** sorgt dafür das `BetterBR` alles Methoden und Instanzvariablen die in `BufferedReader` definiert wurden auch besitzt. (sie werden quasi vereerbt...)

```java
class BetterBR extends BufferedReader{
      ...
}
```

### **`super`-Keyword**

Notwendiger Aufruf des Konstruktors der Superklasse zum

```java
public BetterBR(){
      super (new InputStreamReader(System.in));
}

import java.io.*;
class BetterBR extends BufferedReader {
      public BetterBR(){
            super (new InputStreamReader(System.in));
      }
      public BetterBR(String fileName) throws FileNotFoundException{
            super (new InputStreamReader (new FileInputStream(
                  new File (fileName))));
      }
      public int readInt() throws IOException{
            return Integer.parseInt(super.readLine().trim());
      }
}
```

### **`Protected`-Keyword**

```java
class Figur {
protected String name;
      Figur (String s){ // Konstruktor
            name = s;
      }
      void zeichne(){
            System.out.println (" zeichne "+this);
      }
      void entferne(){
            System.out.println ("entferne "+this);
      }
      public String toString(){
            // fuer Text-Darstellung
            return "Figur: "+name;
      }
}
```

### **Overriding**

Die Klasse Kreis übernimmt alle Methoden der Klasse Figur.
Die Methode toString wird aber durch eine angepasste Version ersetzt.
Diesen Prozess der Ersetzung bzw. Überschreibung von Methoden nennt man Overriding.

```java
class Kreis extends Figur {
      protected Punkt zentrum;
      protected int radius;

      Kreis (String s, int x, int y, int r){// Konstruktor
            super (s);
            zentrum = new Punkt (x,y);
            radius = r;
      }
      public String toString(){ //ueberschriebene Methode
            return "Kreis: "+name+" Zentrum: "+
            zentrum+" Radius: "+radius;
      }
}
```

Möglich weil Kreis abgeleitet von Figur

```java
Figur k = new Kreis ("Otto", 3, 3, 5);
```

## **Polymorphie**

### Ausnutzung der Polymorphie

Wenn Kollektionen von Figur-Objekten verwaltet werden sollen,
können wir die Polymorphie ausnutzen:

```java
Figur[] fa = {
      new Figur ("Anna"),
      new Kreis ("Otto", 3, 3, 5),
      new Rechteck ("Cy", 7, 5, 1) };
for (Figur f: fa) f.entferne ();
```

### Zusammenfassung gemeinsamer Eigenschaften in einer Superklasse

- Wir könnten neben Kreis noch weitere Klassen von Figur ableiten, etwa Rechteck, Dreieck, ...
- Objekte verschiedener Subklassen unterscheiden sich zwar. Gemeinsam an ihrem Verhalten ist aber, dass sie alle die Methoden der Superklasse besitzen.
- Vererbung kann genutzt werden, um gemeinsame Eigenschaften von Subklassen zusammenzufassen.

### Abstrakte Methoden und Klassen (Motivation)

- Die Klasse Figur haben wir eigentlich dafür benutzt, um gemeinsame Eigenschaften ihrer Subklassen zusammenzufassen.
- Darüber hinaus wurde nur auf die Methoden der Klasse `Figur` zugegriffen.
- Was aber können wir tun, wenn wir in der `entferne`-Methode eine Ausgabe der Fläche vorsehen wollen?
- Für eine sinnvolle Methode `flaeche()` ist in dieser Klasse noch zuwenig Information vorhanden. Eine Platzhalter-Methode würde auf jeden Fall von Subklassen **überschrieben** werden.

### **`abstract`-Keyword**

- Es können keine Objekte einer abstrakten Klasse durch new erzeugt werden.
- Für abstrakte Methoden müssen die nicht-abstrakten Subklassen entsprechenden Code enthalten.

```java
abstract class Figur{
      abstract double flaeche(); // hier kein Rumpf
      // Muss von Sub-Klasse implementiert (überschrieben werden)
}
```

## **Interfaces**

Interfaces dienen dazu, ein Verhalten zu spezifizieren, das von Klassen
implementiert werden soll. Eine Klasse kann mehrere Interfaces haben.
Ein Interface drückt Eigenschaften aus, die Klassen in unterschiedlichen Hierarchiestufen implementieren können.

```java
interface Orderable {
      boolean lessThan (Orderable comp);
      boolean equal (Orderable comp);
}
```

- Wenn eine Klasse ein Interface implementiert, kann sie so behandelt werden, als wäre sie eine Subklasse des Interfaces.
- Auch Interfaces können eine Hierarchie bilden.
- Eine implementierende Klasse muss alle Methoden eines implementierten Interfaces und seiner Vorgänger implementieren.
- Ob ein Objekt zu irgendeiner Klasse oder einem Interface gehört (is-a), lässt sich durch einen Ausdruck mit dem Schlüsselwort `instanceof` herausbekommen: Objektname `instanceof` Klasse-oder-Interface


```java
// class SortableInteger implements Orderable implements dies implements das {
class SortableInteger implements Orderable {
      private int val;

      SortableInteger (int val){
            this.val = val; // Konstruktor

      }
      public int intValue(){
            return this.val ; // Wert herausgeben
      }
      public boolean lessThan (Orderable comp){
            return this.val < ((SortableInteger) comp).val;
      }
      public boolean equal (Orderable comp){
            return ((SortableInteger) comp).val == this.val;
      }
      public String toString(){
            
            return new String(""+this.val); // String-Darstellung
      }
}
```

```java
interface EinDimensional{
      public int laenge();
}
interface ZweiDimensional extends EinDimensional{
      public int breite();
}
interface DreiDimensional extends ZweiDimensional{
      public int hoehe();
}
```

### Instanz mehrerer Interfaces

```java
public class Quader implements DreiDimensional,
Comparable<Quader> {
// ... Konstruktoren ...
public int laenge() { return 0; }
public int breite() { return 0; }
public int hoehe() { return 0; }
public int volumen (){
return laenge() * breite() * hoehe();
}
public int compareTo (Quader o){
int me = this.volumen();
int other = o.volumen();
if (me < other) return -1;
if (me > other) return 1;
return 0;
}
```

### Konstanten in Interfaces und Klassen

Interfaces können auch Konstanten `(static final)` definieren.

### Interfaces ohne Inhalt

Interfaces können Methoden, Konstanten, und Felder haben, oder auch leer sein.

### Interface-Implementierung durch anonyme Klasse

```java
public static void main (String[] args){
      plot (new D2Method() {// implementiert D2Method
                  public double compute (double value){
                  return value*value;
                  } // end compute
            } // end anonyme Klasse
      ); // end plot-Statement
} // end main
```

### Designentscheidung: Interface oder abstrakte Klasse

### Interface mit Standard-Implementierung


## dynamisches binden