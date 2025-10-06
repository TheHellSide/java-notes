# VARIABILI
Una **variabile** è un contenitore che memorizza un valore. In Java, devi **dichiarare** il tipo della variabile prima di usarla.

```java
int numero = 10;             // intero
double prezzo = 5.99;        // numero decimale
boolean attivo = true;       // booleano (true o false)
String nome = "Mario";       // stringa di testo
```

---
##### PARSING
Il **parsing** è la **conversione di un dato da un tipo all'altro**, per esempio da una `String` a un `int`.

```java
String s = "42";
int x = Integer.parseInt(s);

String s = "true";
boolean valore = Boolean.parseBoolean(s);  // restituisce true

double d = 9.99;
int i = (int) d;  // i vale 9 (perde la parte decimale)
```

