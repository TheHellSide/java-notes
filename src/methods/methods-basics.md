# METODI
Un **metodo** in Java è un **blocco di codice** che esegue una determinata azione e può essere **chiamato** (invitato) ogni volta che serve, evitando di riscrivere lo stesso codice più volte.

> In parole semplici: un metodo è come una **funzione** in matematica o in altri linguaggi di programmazione.

```java
[modificatore] tipoRitorno nomeMetodo(parm1, parm2, ...) {
    // corpo del metodo
    return valore;  // solo se il tipoRitorno non è void
}
```

---
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