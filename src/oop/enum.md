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