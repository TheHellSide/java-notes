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