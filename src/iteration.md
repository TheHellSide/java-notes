# ITERAZIONE
L’**iterazione** è un concetto fondamentale nella programmazione: rappresenta il **processo di ripetere un insieme di istruzioni più volte**, fino a quando una determinata **condizione logica** è soddisfatta, oppure per un **numero predefinito di volte**.

> In parole semplici, l’iterazione consente a un programma di **“fare qualcosa più volte”** senza dover scrivere più volte lo stesso codice.  

---
### WHILE
Il ciclo **`while`** ripete un blocco di istruzioni **finché la condizione specificata risulta vera**.

> Se la condizione è _falsa sin dall’inizio_, il blocco di codice **non viene eseguito nemmeno una volta**.

**Sintassi:**
```java
while (condizione) {
	// istruzioni da eseguire 
}
```

**Esempio:**
1. Viene inizializzata la variabile `i = 0`.
2. Si controlla la condizione `i < 5`.
3. Se è vera, si esegue il blocco tra parentesi graffe.
4. Alla fine di ogni ciclo, `i` viene incrementato (`i++`).
5. Quando `i` diventa 5, la condizione è falsa → il ciclo termina.

```java 
int i = 0;

while (i < 5) {
	System.out.println("Valore di i: " + i);
	i++; 
}```

> **Uso tipico:** quando **non si sa esattamente quante volte** bisogna ripetere le istruzioni, ma si vuole continuare finché una condizione è vera.

---

### DO-WHILE
Il ciclo **`do-while`** è simile al `while`, ma con una **differenza importante**:

> Il blocco di codice viene **eseguito almeno una volta**, anche se la condizione è falsa fin dall’inizio.

**Sintassi:**
```java
do {     
	// istruzioni da eseguire 
} 
while (condizione);
```

**Esempio:**
- Il codice dentro `do { ... }` viene eseguito una prima volta **senza controllare la condizione**.
- Poi la condizione (`i < 3`) viene valutata:
    - se è vera, il ciclo continua;
    - se è falsa, termina.

```java
int i = 0;  

do { 
    System.out.println("i vale: " + i); 
	i++; 
} 
while (i < 3);
```

> **Uso tipico:** quando si vuole **eseguire il corpo del ciclo almeno una volta**, ad esempio per chiedere un input all’utente e poi controllare se è valido (e. crud-operations).

---
### FOR
Il ciclo **`for`** viene usato quando si sa **esattamente quante volte** si vuole ripetere un’operazione.

**Sintassi:**
```java
for (inizializzazione; condizione; incremento) {     
	// istruzioni da ripetere 
}
```

**Esempio:**
1. `int i = 0` → inizializzazione (eseguita una sola volta).
2. `i < 5` → condizione che decide se il ciclo continua.
3. `i++` → incremento dopo ogni iterazione.
4. Il blocco viene ripetuto finché la condizione rimane vera.

```java
for (int i = 0; i < 5; i++) { 
    System.out.println("i = " + i); 
}
```

> **Uso tipico:** quando si ha un numero noto di iterazioni (es. “ripeti 10 volte”, “scorri un array da 0 a n-1”).

---
### FOR-EACH
Il ciclo **`for-each`** è una forma semplificata del `for` che permette di **scorrere direttamente gli elementi** di una collezione (come `ArrayList`).

**Sintassi:**
```java
for (TipoElemento variabile : collezione) {     
	// usa direttamente variabile
}
```

**Esempio:**
- Alla prima iterazione, `nome` vale `"Luca"`.
- Alla seconda, `nome` vale `"Anna"`.
- Alla terza, `"Marco"`.
- Il ciclo termina quando ha attraversato tutti gli elementi dell’array.

```java
String[] nomi = {"Luca", "Anna", "Marco"};  

for (String nome : nomi) { 
    System.out.println("Ciao " + nome); 
}
```

> **Uso tipico:** perfetto per **leggere o elaborare ogni elemento di una collezione**, senza modificare l’indice o preoccuparsi dei limiti dell’array.