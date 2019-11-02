# Java Cheat Sheet

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

```java

```
