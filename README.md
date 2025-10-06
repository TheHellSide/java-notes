# Java
**Java** è un linguaggio di programmazione orientato agli oggetti, creato da **Sun Microsystems** nel 1995 (ora di proprietà di **Oracle**). È noto per essere **portabile**, **sicuro** e **versatile**.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
### Perché è così importante:

- **Portabilità**: Java è "write once, run anywhere" (scrivi una volta, esegui ovunque) grazie alla **Java Virtual Machine (JVM)**, che permette di eseguire il codice Java su qualsiasi sistema operativo senza modifiche.
- **Affidabilità**: È ampiamente usato in sistemi aziendali, banche, applicazioni Android, e backend di siti web per la sua stabilità e robustezza.
- **Sicurezza**: Include funzionalità integrate per ridurre rischi e vulnerabilità nei programmi.

> In breve, Java è importante perché combina **portabilità**, **prestazioni** e **affidabilità**, rendendolo un pilastro nello sviluppo software a livello mondiale.

---
### VARIABILI:
Una **variabile** è un contenitore che memorizza un valore. In Java, devi **dichiarare** il tipo della variabile prima di usarla.

```java
int numero = 10;             // intero
double prezzo = 5.99;        // numero decimale
boolean attivo = true;       // booleano (true o false)
String nome = "Mario";       // stringa di testo
```

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

---
### SELEZIONE:
**Definizione**:  
La **selezione** è il meccanismo che consente a un programma di **scegliere tra diverse strade** in base a una condizione.

> In pratica, è il modo in cui un programma dice: **"se succede questo, fai quello"**, altrimenti fai qualcos'altro.
##### IF (condizione semplice)
Esegue il blocco **solo se** la condizione è vera.

```java
int numero = 10;

if (numero > 0) {
    System.out.println("Il numero è positivo");
}
```

##### IF - ELSE
Sceglie tra due blocchi: uno se è **vero**, l’altro se è **falso**.

```java
int numero = -5;

if (numero >= 0) {
    System.out.println("Positivo");
} 
else {
    System.out.println("Negativo");
}
```

##### IF - ELSE IF - ELSE
Permette più controlli, in ordine.

```java
int voto = 75;

if (voto >= 90) {
    System.out.println("Ottimo");
} 
else if (voto >= 70) {
    System.out.println("Buono");
} 
else if (voto >= 50) {
    System.out.println("Sufficiente");
} 
else {
    System.out.println("Insufficiente");
}
```

##### SWITCH
Alternativa compatta all’`if-else` per **valori precisi** (tipi `int`, `char`, `String`, `enum`...).

```java
int giorno = 3;

switch (giorno) {
    case 1:
        System.out.println("Lunedì");
        break;
    case 2:
        System.out.println("Martedì");
        break;
    case 3:
        System.out.println("Mercoledì");
        break;
    default:
        System.out.println("Giorno non valido");
}
```

> `break`: serve per **uscire** dallo `switch` (altrimenti continua).
> `default`: è come `else`: viene eseguito se nessun caso corrisponde.

---
### ITERAZIONE:
L’**iterazione** è il processo di **ripetere un blocco di istruzioni** più volte, finché una condizione è vera o per un numero stabilito di volte.

> In pratica, è il modo in cui un programma **"fa un ciclo"** su un insieme di istruzioni.

##### WHILE
Esegue il blocco **finché** la condizione è vera.

```java
int i = 0;

while (i < 5) {
    System.out.println("Valore di i: " + i);
    i++;
}
```

##### DO-WHILE
Come `while`, **ma esegue almeno una volta** il codice anche se la condizione è falsa.

```java
int i = 0;

do {
    System.out.println("i vale: " + i);
    i++;
} 
while (i < 3);
```

##### FOR (Classico)
Utile quando sai **quante volte** iterare.

```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

> Struttura: `for (inizializzazione; condizione; incremento)`

##### FOR-EACH (iterativo su array o collezioni)
Serve per **scorrere direttamente elementi** di un array o lista, senza usare indici.

```java
String[] nomi = {"Luca", "Anna", "Marco"};

for (String nome : nomi) {
    System.out.println("Ciao " + nome);
}
```

---
# OOP (Object Oriented Programming):
**OOP** (Object-Oriented Programming) significa **Programmazione Orientata agli Oggetti**.  
È un **modo di scrivere codice** che si basa su **oggetti**, che rappresentano **cose del mondo reale** (es. una persona, una macchina, un conto bancario) e contengono **dati** e **funzionalità**.

### CLASSI e OGGETTI
-  ***CLASSE***
	Una **classe** è un **modello** (o **stampino**) per creare oggetti.  
	Definisce **che dati ha un oggetto** (attributi) e **cosa può fare** (metodi).
	
```java
	public class Persona {
	    String nome;
	    int eta;
	
	    void saluta() {
	        System.out.println("Ciao, mi chiamo " + nome);
	    }
	}
```

-  ***OGGETTO***
	Un **oggetto** è un’**istanza di una classe**, cioè un elemento concreto **creato a partire da una classe**.
	
```java
	Persona p1 = new Persona();   // creo un oggetto
	p1.nome = "Luca";             // assegno valore all’attributo
	p1.eta = 25;
	p1.saluta();                  // uso un metodo
```

-  ***ATTRIBUTO***
	Un **attributo** (o **campo**) è una **variabile** dichiarata dentro una classe.  
	Contiene le **informazioni** di un oggetto.
	
```java
	String nome;   // attributo
	int eta;       // attributo
```

-  ***METODO***
	Un **metodo** è una **funzione** dentro una classe.  
	Serve a definire il **comportamento** dell’oggetto, cioè **cosa può fare**.
	
```java
	void saluta() {
	    System.out.println("Ciao, mi chiamo " + nome);
	}
```

---
### COSTRUTTORE
Un **costruttore** è un **metodo speciale** di una classe che viene chiamato **automaticamente** quando crei un nuovo oggetto (con `new`).  
Serve a **inizializzare** gli attributi dell’oggetto al momento della sua creazione.
##### CARATTERISTICHE PRINCIPALI:
- Ha **lo stesso nome** della classe.
- **Non ha un tipo di ritorno** (nemmeno `void`).
- Può ricevere **parametri** per impostare valori iniziali.
- Puoi definire **più costruttori** (overloading), con parametri diversi.

```java
public class Persona {
    String nome;
    int eta;
	
    // costruttore
    public Persona(String nome, int eta) {
        this.nome = nome;
        this.eta = eta;
    }
}

public class Main {
    public static void main(String[] args) {
        Persona p = new Persona("Anna", 30);  // inizializza nome e eta subito
        System.out.println(p.nome);  // Output: Anna
        System.out.println(p.eta);   // Output: 30
    }
}
```

---
### TO_STRING
`toString()` è un **metodo speciale** definito nella classe base `Object` (tutte le classi Java ereditano da `Object`), che serve a **ritornare una rappresentazione testuale (stringa) di un oggetto**.

> ***Perché è importante?***
> Quando usi un oggetto in un contesto dove serve una stringa (es. dentro `System.out.println()`), Java chiama automaticamente il suo `toString()`.

```java
public class Persona {
    String nome;
    int eta;

    public Persona(String nome, int eta) {
        this.nome = nome;
        this.eta = eta;
    }

    @Override
    public String toString() {
        return "Persona[nome=" + nome + ", eta=" + eta + "]";
    }
}
```

```java
public class Main {
	public static void main (String [] args) {
		Persona p = new Persona("Luca", 25);
		System.out.println(p);
		// Output: Persona[nome=Luca, eta=25]
	}
}
```

---
### MODIFICATORI DI ACCESSO
I modificatori di accesso servono a **controllare la visibilità** di classi, metodi e variabili, cioè chi può usarli o vederli nel programma.

-  ***PUBLIC***
	**Public** è un modificatore di accesso che rende classi, metodi o variabili accessibili da qualsiasi altra classe, indipendentemente dal pacchetto in cui si trovano. Se un elemento è dichiarato public, può essere utilizzato ovunque nel progetto.
	
```java
	public class Esempio {
	    public int numero;
	    public void metodo() {}
	}
```

-  ***PRIVATE***
	**Private** è un modificatore che limita la visibilità di metodi o variabili solo all’interno della classe in cui sono dichiarati. Nessun altro codice esterno a quella classe può accedere direttamente a membri privati, garantendo così l’incapsulamento e la protezione dei dati.
	
```java
	public class Esempio {
	    private int numero;
	    private void metodo() {}
	}
```

- ***PROTECTED***
	**Protected** permette l’accesso a metodi e variabili da parte della stessa classe, da tutte le classi dello stesso pacchetto e dalle sottoclassi anche se si trovano in pacchetti differenti. Questo modificatore è utile per ereditare comportamenti mantenendo un certo grado di protezione.
	
```java
	public class Esempio {
	    protected int numero;
	    protected void metodo() {}
	}
```

> Quando non viene specificato alcun modificatore di accesso, si parla di visibilità di default o package-private. In questo caso, classi, metodi o variabili sono accessibili solamente all’interno del pacchetto in cui sono dichiarati e non da classi esterne a quel pacchetto.

```java
class Esempio {   // visibile solo nel pacchetto
    int numero;   // visibile solo nel pacchetto
    void metodo() {}
}
```

---
### INCAPSULAMENTO
**Incapsulamento** è il principio di nascondere i dettagli interni di un oggetto e di proteggere i dati. Significa che gli attributi di una classe sono generalmente dichiarati privati e possono essere modificati o letti solo tramite metodi pubblici detti getter e setter. Questo permette di controllare l’accesso ai dati, migliorare la sicurezza e mantenere l’integrità dello stato dell’oggetto.

```java
public class Persona {
    private String nome;  // attributo privato
	
    public String getNome() {
        return nome;      // getter per leggere il nome
    }
	
    public void setNome(String nome) {
        this.nome = nome; // setter per modificare il nome
    }
}
```

---
### EREDITARIETÀ
**Ereditarietà** è il meccanismo attraverso il quale una classe (detta sottoclasse o classe derivata) può estendere un’altra classe (detta superclasse o classe base), ereditando i suoi attributi e metodi. Questo favorisce il riuso del codice e la creazione di gerarchie di classi, permettendo alle sottoclassi di specializzare o modificare il comportamento ereditato.

```java
public class Animale {
    public void verso() {
        System.out.println("Verso generico");
    }
}

public class Cane extends Animale {
    @Override
    public void verso() {
        System.out.println("Bau Bau");
    }
}
```

---
### POLIMORFISMO
**Polimorfismo** significa "molte forme" e indica la capacità di oggetti di classi diverse di rispondere allo stesso messaggio (cioè chiamata a un metodo) in modi diversi. In Java, questo si realizza tramite l’overriding dei metodi nelle sottoclassi o tramite l’uso di classi e interfacce che condividono un tipo comune, permettendo di scrivere codice più flessibile e generico.

```java
// Classe base
class Animale {
    public void verso() {
        System.out.println("Verso generico");
    }
}

// Sottoclasse 1
class Cane extends Animale {
    @Override
    public void verso() {
        System.out.println("Bau Bau");
    }
}

// Sottoclasse 2
class Gatto extends Animale {
    @Override
    public void verso() {
        System.out.println("Miao Miao");
    }
}

public class Main {
    public static void main(String[] args) {
        Animale[] animali = { new Cane(), new Gatto(), new Animale() };

        for (Animale a : animali) {
            a.verso();  // Il metodo chiamato dipende dall’oggetto
        }
    }
}

```

---
### ASTRAZIONE
**Astrazione** è il processo di focalizzarsi sugli aspetti essenziali di un oggetto ignorandone i dettagli non rilevanti. In pratica, si definiscono classi o interfacce che specificano cosa fa un oggetto senza dire come lo fa. Questo aiuta a ridurre la complessità e a separare l’interfaccia dalla sua implementazione.

```java
public abstract class Forma {
    public abstract double area();  // metodo astratto senza corpo
}

public class Cerchio extends Forma {
    private double raggio;

    public Cerchio(double raggio) {
        this.raggio = raggio;
    }
	
    @Override
    public double area() {
        return Math.PI * raggio * raggio;
    }
}
```

---
### INTERFACCE
**Interfacce** in Java sono un tipo di classe astratta pura che definisce solo i metodi senza implementazione. Le classi che “implementano” un’interfaccia devono fornire il codice concreto per tutti i metodi dichiarati. Le interfacce permettono di definire contratti comuni che classi diverse possono rispettare, facilitando la programmazione orientata ai servizi e l’uso del polimorfismo.

```java
public interface Volante {
    void vola();
}

public class Uccello implements Volante {
    @Override
    public void vola() {
        System.out.println("Sto volando!");
    }
}
```

---
### ENUM
`enum` (abbreviazione di _enumeration_) è un tipo speciale di classe in Java che serve a definire un insieme di **valori costanti e fissi**.  
Gli enum sono utili quando vuoi rappresentare una lista limitata e predefinita di opzioni, come giorni della settimana, stati di un processo, colori, ecc.

##### CARATTERISTICHE PRINCIPALI
- Ogni valore definito in un enum è un **istanza dell’enum stesso**.
- Gli enum sono tipi sicuri (type-safe), cioè non puoi assegnare valori diversi da quelli definiti.
- Possono avere attributi, metodi e costruttori propri, come una classe normale.

```java
enum Giorno {
    LUNEDI, MARTEDI, MERCOLEDI, GIOVEDI, VENERDI, SABATO, DOMENICA
}

public class Main {
	public static void main (String [] args) {
		Giorno oggi = Giorno.LUNEDI;
		
		if (oggi == Giorno.LUNEDI) {
		    System.out.println("Inizia la settimana!");
		}
	}
}
```

> ***VANTAGGI DEGLI ENUM***
> - Evitano errori dovuti a valori sbagliati o stringhe scritte male.
> - Migliorano la leggibilità e manutenzione del codice.
> - Possono essere usati in `switch` come costanti.

---
# METODI
Un **metodo** in Java è un **blocco di codice** che esegue una determinata azione e può essere **chiamato** (invitato) ogni volta che serve, evitando di riscrivere lo stesso codice più volte.

> In parole semplici: un metodo è come una **funzione** in matematica o in altri linguaggi di programmazione.

```
[modificatore] tipoRitorno nomeMetodo(parm1, parm2, ...) {
    // corpo del metodo
    return valore;  // solo se il tipoRitorno non è void
}
```
##### A COSA SERVE UN METODO?
Un metodo serve per:
- organizzare il codice in blocchi riutilizzabili;
- suddividere il lavoro in compiti più piccoli;
- rendere il programma più ordinato e comprensibile;
- ricevere input (parametri), elaborare e restituire output (valore di ritorno).

```java
public class Matematica {

    public int somma(int a, int b) {
        return a + b;
    }

    public void stampaMessaggio() {
        System.out.println("Benvenuto nel programma!");
    }

    public static void main(String[] args) {
        Matematica m = new Matematica();

        m.stampaMessaggio();
        int risultato = m.somma(3, 4);
        System.out.println("Somma: " + risultato);
    }
}
```

---
# THREADS
Un **thread** è una **unità di esecuzione separata** all’interno di un programma.  
In pratica, un thread permette di **eseguire più operazioni allo stesso tempo**.

Java consente di creare **programmi multithread**, in cui più thread vengono eseguiti in parallelo. Questo è utile, ad esempio, per scaricare dati mentre l'interfaccia grafica rimane attiva, o per gestire più utenti contemporaneamente in un server.

> ***PERCHÉ USARE I THREAD?***
> Un’applicazione monothread esegue una sola cosa alla volta.  
> 
> Con i thread puoi:
> - eseguire **operazioni lente in background** senza bloccare tutto il programma;
> - **ottimizzare** l’uso della CPU su computer multi-core;
> - **separare compiti diversi** (es. calcoli, interfaccia, rete).

### CREARE UN THREAD
-  ***Estendere la classe `Thread`***
	creare un thread estendendo la classe `Thread` consiste nel derivare una nuova classe e ridefinire il metodo `run()`, che conterrà il codice da eseguire in parallelo. Il thread parte quando si chiama il metodo `start()` sull’oggetto creato.
	
```java
	public class MioThread extends Thread {
	    @Override
	    public void run() {
	        System.out.println("Thread in esecuzione!");
	    }
		
	    public static void main(String[] args) {
	        MioThread t = new MioThread();
	        t.start();  // NON usare run(), ma start()
	    }
	}
```

- ***Implementare l'interfaccia `Runnable`***
	creare un thread implementando l’interfaccia `Runnable` consiste nel definire una classe che contiene il metodo `run()` e passare un’istanza di essa a un oggetto `Thread`. Il codice all’interno di `run()` verrà eseguito in un nuovo thread dopo la chiamata a `start()`.
	
```java
	public class MioRunnable implements Runnable {
	    @Override
	    public void run() {
	        System.out.println("Runnable in esecuzione!");
	    }
		
	    public static void main(String[] args) {
	        Thread t = new Thread(new MioRunnable());
	        t.start();
	    }
	}
```
