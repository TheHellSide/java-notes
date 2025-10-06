# Problemi di Concorrenza in Java
I **problemi di concorrenza** si verificano quando più thread **accedono o modificano risorse condivise** senza un corretto controllo.  
Questo può causare **risultati sbagliati, blocchi, o comportamenti imprevedibili nel programma**.

---
### 🌀 1. Race Condition
Due thread modificano la **stessa variabile contemporaneamente**. Il risultato finale è **imprevedibile**.

```java 
class Counter {
	int value = 0;   
	   
	void increment() {         
		value++; // NON ATOMICO!     
	}
}
```

🛠️ **Soluzioni e spiegazioni:**

- **`synchronized`**: permette di bloccare l’accesso al metodo o blocco di codice a un solo thread alla volta, garantendo mutua esclusione e visibilità immediata delle modifiche.

```java
synchronized void increment() {     
	value++; 
}
```

- **`AtomicInteger`**: classe che fornisce operazioni atomiche su interi senza sincronizzazione esplicita, usando istruzioni CPU speciali per evitare race condition in modo efficiente.

```java
import java.util.concurrent.atomic.AtomicInteger;

AtomicInteger value = new AtomicInteger(0);  
void increment() {     
	value.incrementAndGet(); 
}
```

---
### 😵‍💫 2. Visibilità incoerente

Un thread **non vede gli aggiornamenti** fatti da un altro su una variabile perché le modifiche possono restare in cache o non essere immediatamente visibili.

```java
boolean isReady = false; 
while (!isReady) {     
	// potrebbe non uscire mai
}
```

🛠️ **Soluzione: `volatile`**

- **`volatile`** garantisce che la variabile sia letta e scritta direttamente nella memoria principale, evitando cache incoerenti. Assicura visibilità immediata tra thread ma non mutua esclusione.

```java
volatile boolean isReady = false;
```

---
### 🔒 3. Deadlock

Due thread aspettano **l’uno l’altro** per rilasciare un lock → si **bloccano per sempre**.

#Thread_1:

```java
synchronized(obj1) {     
	synchronized(obj2) {
		... 
	} 
}
```

#Thread_2:

```java
synchronized(obj2) {     
	synchronized(obj1) { 
		... 
	} 
}
````

🛠️ Soluzione: **ordinare sempre i lock** nello stesso ordine

---

### 🕳️ 4. Starvation

Un thread **non ottiene mai tempo CPU** perché altri thread più “forti” lo sovrastano.

🛠️ Soluzione: evitare lock lunghi, usare thread bilanciati

---

### 🔁 5. Livelock

I thread lavorano ma **non progrediscono**, es. si cedono continuamente il controllo.

🛠️ Soluzione: attese casuali o limiti ai tentativi