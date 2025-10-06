### SELEZIONE
La **selezione** è uno dei concetti fondamentali della programmazione strutturata.  
Serve per permettere a un programma di **scegliere tra diverse alternative di esecuzione** in base a una o più **condizioni logiche**.

> In parole semplici: è il modo con cui un programma "decide cosa fare" a seconda della situazione.

---
### IF (condizione semplice)
Il costrutto `if` consente di **eseguire un blocco di istruzioni solo se** una condizione è vera (`true`).

**Sintassi:**
```java
if (condizione) {
    // istruzioni da eseguire se la condizione è vera
}
```

**Esempio:**
1. Il programma controlla la condizione `numero > 0`.
2. Se la condizione è vera, esegue il blocco dentro le graffe.
3. Se è falsa, **salta** quel blocco e continua con le istruzioni successive.

```java
int numero = 10;

if (numero > 0) {
    System.out.println("Il numero è positivo");
}
```

> 💡 **Uso tipico:** controllare una condizione singola, come verificare se un numero è positivo, se un file esiste, se l’utente è autenticato, ecc.

---
### IF-ELSE
Il costrutto `if-else` permette di **scegliere tra due alternative**:  
- una viene eseguita **se la condizione è 'true'**,  
- l’altra **se è 'false'**.

**Sintassi:**
```java
if (condizione) {
    // blocco eseguito se condizione è vera
} else {
    // blocco eseguito se condizione è falsa
}
```

**Esempio:**
- Se `numero >= 0` è vero, viene stampato “Positivo”.
- Altrimenti, viene eseguito il blocco `else` e viene stampato “Negativo”.

```java
int numero = -5;

if (numero >= 0) {
    System.out.println("Positivo");
} else {
    System.out.println("Negativo");
}
```

> **Uso tipico:** quando si deve gestire un **caso alternativo**, come "pari" o "dispari".
> **OPERATORE TERNARIO:** condizione ? codice_condizione_vera : codice_condizione_falsa;

---
### ELSE-IF
Quando serve **valutare più condizioni diverse**, una dopo l’altra, si può usare la catena `if - (else if * n) - else`.

**Sintassi:**
```java
if (condizione1) {
    // se condizione1 è vera
} else if (condizione2) {
    // se condizione1 è falsa ma condizione2 è vera
    //...
} else {
    // se nessuna condizione precedente è vera
}
```

**Esempio:**
- Il programma verifica le condizioni **in ordine** dall’alto verso il basso.  
- Appena ne trova una vera, **esegue quel blocco** e **salta i successivi**.  
- Se nessuna è vera, viene eseguito l’`else` finale (opzionale).

```java
int voto = 75;

if (voto >= 90) {
    System.out.println("Ottimo");
} else if (voto >= 70) {
    System.out.println("Buono");
} else if (voto >= 50) {
    System.out.println("Sufficiente");
} else {
    System.out.println("Insufficiente");
}
```

> **Uso tipico:** quando si vuole classificare un valore o gestire **più scenari possibili** (ad esempio: voto, temperatura, età, punteggio, ecc.).

---
### SWITCH
Il costrutto `switch` è un’alternativa compatta e leggibile al `if-else` quando si devono **confrontare valori precisi e discreti**.

**Sintassi:**
```java
switch (espressione) {
    case valore1:
        // istruzioni se espressione == valore1
        break;
    case valore2:
        // istruzioni se espressione == valore2
        break;
    ...
    default:
        // istruzioni se nessun valore corrisponde
}
```

**Esempio:**
- Il valore di `giorno` viene confrontato con ciascun `case`.
- Quando trova una corrispondenza (`giorno == 3`), esegue il blocco relativo.
- L’istruzione `break` serve per **interrompere il flusso** del `switch`, evitando che vengano eseguiti anche i casi successivi (“fall-through”).
- Se nessun `case` corrisponde, viene eseguito il blocco `default`.

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

> **Uso tipico:** scegliere un’azione in base a un **valore numerico o testuale preciso**, come il giorno della settimana, un comando inserito, un menu di opzioni, ecc.
