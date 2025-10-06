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