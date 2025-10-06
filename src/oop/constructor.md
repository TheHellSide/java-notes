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