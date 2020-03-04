# **Heinz Cheat Sheet**

- [**Heinz Cheat Sheet**](#heinz-cheat-sheet)
  - [**Was ist Informatik?**](#was-ist-informatik)
    - [Aspekte der Informatik](#aspekte-der-informatik)
    - [Was ist ein Computer](#was-ist-ein-computer)
    - [Was ist eigentlich ein Programm](#was-ist-eigentlich-ein-programm)
  - [**Programmierparadigmen, ein fundamentaler Programmier-Stile**](#programmierparadigmen-ein-fundamentaler-programmier-stile)
    - [Warum Java](#warum-java)
  - [**Programme in Java**](#programme-in-java)
    - [Das Compiler-Modell](#das-compiler-modell)
    - [Das Interpreter-Modell](#das-interpreter-modell)
    - [Das Java-Modell](#das-java-modell)

## **Was ist Informatik?**

**Informatik lt. Duden:**
Ist die Wissenschaft von der automatischen Verarbeitung von Informationen, besonders der automatischen Verarbeitung mit Hilfe von Digitalrechnern.

**Association of Computing Machinery (ACM):**  
Computer science is the systematic study of algorithms and data structures,
specifically

- their formal properties,
- their mechanical and linguistic realizations, and
- their applications

### Aspekte der Informatik

- Technische Realisierung
- Effiziente Verfahren
- Theorie
- Programmiersprachen
- Techniken und Tools zur Programmentwicklung

### Was ist ein Computer

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

## **Programme in Java**

Um ein Programm auf einem Rechner ausführen zu können, müssen wir

1. das Programm für den Computer zugänglich machen,
2. das Programm in eine Form übersetzen, die der Rechner versteht, und
3. den Computer anweisen, das Programm auszuführen.

### Das Compiler-Modell

Das Programm wird direkt in Maschinencode übersetzt und kann vom Rechner unmittelbar ausgeführt werden.

### Das Interpreter-Modell

- Das Programm wird von einem Interpreter direkt ausgeführt.
- Der Interpreter verwendet für jedes Statement bei der Ausführung eine entsprechende Sequenz von Maschinenbefehlen.

Vergleich zum Compiler:

1. Das Programm muss nicht erst komplett übersetzt werden.
2. Die Interpretation ist langsamer als die Ausführung kompilierter Programme.

### Das Java-Modell

Java verwendet einen Interpreter und einen Compiler:

- Java übersetzt zunächst in eine **Bytecode** genannte Zwischensprache: `javac Program1.java`
- Der Bytecode wird dann von der **Java virtual machine (JVM) interpretiert**: `java Program1`

```txt
                                                   -------------------------------------
                                                   |                                   |
--------------     ---------    ---------------    | ---------------     ------------- |
| Hello.java |  -> | javac | -> | Hello.class | -> | | Interpreter | <-> | Prozessor | |
--------------     --------     ---------------    | ---------------     ------------- |
                                                   |                                   |
                                                   -------------------------------------
```

Ein Komplettes Programm

```java
public class Program1 {
    public static void main (String[ ] arg) {
        System.out.println ("This is my first Java program");
        System.out.println (" but it won't be my last.");
    }
}
```

**Programme modellieren die Realität**  
Modelle sind (vereinfachende) Darstellungen realer Systeme und Zusammenhänge. Sie enthalten die relevanten Eigenschaften in  modellierten Objekten.
  
- Elemente eines Modells **repräsentieren** andere, komplexe Dinge. (Objekte)
- Die Elemente eines Modells haben ein bestimmtes, konsistentes Verhalten. (Klassen)
- Die Elemente eines Modells können entsprechend ihrem Verhalten zu verschiedenen Gruppen zusammengefasst werden. (Namespaces)
- Externe Aktionen stoßen das Verhalten eines Model an. (Methoden)

**Objekte in Java**  
Java verwendet für die Elemente eines Modelles ***Objekte***.  

**Klassen in Java**  
Kategorien von Elementen eines Modells heißen in Java **Klassen**

**Räpresentation in Java**  
Namen einer Klasse oder einer Methode in Java nennt man Identifier oder Bezeichner
Klassen und Nachrichten müssen einen Bezeichner haben. Dabei wird zwischen Groß- und Kleinschreibung unterschieden.

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

Eine **Referenz** in Java ist ein Ausdruck, der einen Bezug zu einem **Objekt** herstellt.
`System.out` referenziert ein Objekt der Klasse `PrintStream`, welches den Monitor modelliert.  
`System.out` ist also eine **Referenz auf das `PrintStream`-Objekt**.

**Nachrichten in Java**  
Durch Nachrichten aktiviert man das Verhalten eines Objektes, das in Seiner Klasse vordefiniert wurde.  
Schickt man eine **`println`-Nachricht an das Objekt der Klasse `PrintStream`**, wird ein Text auf dem Bildschirm ausgegeben.
Das Verhalten, dass ausgelöst wird, stellt die Klasse `PrintStream` zur Verfügung.
Es handelt sich hierbei um einen **Methoden-Aufruf**.  
Der Code der die Nachricht gesendet (die Methode aufgerufen) hat wird so lange nicht weiter ausgeführt, bis das Verhalten dass die Nachricht ausgelöst hat abgearbeitet ist.

**Komponenten einer Nachricht**

- **Empfänger**: Die Referenz auf das Empfänger-Objekt zB. `System.out` gefolgt von einem Punkt
- **Methodenselektor**: Der Name des vordefinierten Verhaltens des Objektes zB. `print`, `println`
- **Details**: Die weiteren Informationen die in Klammer eingeschlossen werden zB. `("Argument")`

Hier am Beispiel: `System.out.println("Argument");`

```Java
System.out. // Empfänger, Referenz auf ein Objekt der Klasse print Stream
println("Argument") // Stellt die gesammte Nachricht dar
println()   // Das Verhalten, die vordefinierte Methode
"Argument"  // Details der Nachricht, auch Argument genannt
```
