# THREADS
Un **thread** è una **unità di esecuzione separata** all’interno di un programma.  
In pratica, un thread permette di **eseguire più operazioni allo stesso tempo**.

Java consente di creare **programmi multithread**, in cui più thread vengono eseguiti in parallelo. Questo è utile, ad esempio, per scaricare dati mentre l'interfaccia grafica rimane attiva, o per gestire più utenti contemporaneamente in un server.

> ***PERCHÉ USARE I THREAD?***
> Un’applicazione monothread esegue una sola cosa alla volta.  
> 
> Con i thread puoi:
> - eseguire **operazioni lente in background** senza bloccare tutto il programma;
> - **ottimizzare** l’uso della CPU su computer multi-core;
> - **separare compiti diversi** (es. calcoli, interfaccia, rete).

---
### CREARE UN THREAD
-  ***Estendere la classe `Thread`***
	creare un thread estendendo la classe `Thread` consiste nel derivare una nuova classe e ridefinire il metodo `run()`, che conterrà il codice da eseguire in parallelo. Il thread parte quando si chiama il metodo `start()` sull’oggetto creato.
	
```java
	public class MioThread extends Thread {
	    @Override
	    public void run() {
	        System.out.println("Thread in esecuzione!");
	    }
		
	    public static void main(String[] args) {
	        MioThread t = new MioThread();
	        t.start();  // NON usare run(), ma start()
	    }
	}
```

- ***Implementare l'interfaccia `Runnable`***
	creare un thread implementando l’interfaccia `Runnable` consiste nel definire una classe che contiene il metodo `run()` e passare un’istanza di essa a un oggetto `Thread`. Il codice all’interno di `run()` verrà eseguito in un nuovo thread dopo la chiamata a `start()`.
	
```java
	public class MioRunnable implements Runnable {
	    @Override
	    public void run() {
	        System.out.println("Runnable in esecuzione!");
	    }
		
	    public static void main(String[] args) {
	        Thread t = new Thread(new MioRunnable());
	        t.start();
	    }
	}
```