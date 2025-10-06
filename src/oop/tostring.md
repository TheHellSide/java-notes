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