# OOP (Object Oriented Programming):
**OOP** (Object-Oriented Programming) significa **Programmazione Orientata agli Oggetti**.  
È un **modo di scrivere codice** che si basa su **oggetti**, che rappresentano **cose del mondo reale** (es. una persona, una macchina, un conto bancario) e contengono **dati** e **funzionalità**.

---
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
	Persona p1 = new Persona(); // creo un oggetto
	p1.nome = "Luca"; / assegno valore all’attributo
	p1.eta = 25;
	p1.saluta(); // uso un metodo
```

-  ***ATTRIBUTO***
	Un **attributo** (o **campo**) è una **variabile** dichiarata dentro una classe.  
	Contiene le **informazioni** di un oggetto.
	
```java
	String nome;   // attributo
	int eta;
```

-  ***METODO***
	Un **metodo** è una **funzione** dentro una classe.  
	Serve a definire il **comportamento** dell’oggetto, cioè **cosa può fare**.
	
```java
	void saluta() {
	    System.out.println("Ciao, mi chiamo " + nome);
	}
```
