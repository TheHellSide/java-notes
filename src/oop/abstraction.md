### ASTRAZIONE
**Astrazione** è il processo di focalizzarsi sugli aspetti essenziali di un oggetto ignorandone i dettagli non rilevanti. In pratica, si definiscono classi o interfacce che specificano cosa fa un oggetto senza dire come lo fa. Questo aiuta a ridurre la complessità e a separare l’interfaccia dalla sua implementazione.

```java
public abstract class Forma {
    public abstract double area();  // metodo astratto senza corpo
}

public class Cerchio extends Forma {
    private double raggio;

    public Cerchio(double raggio) {
        this.raggio = raggio;
    }
	
    @Override
    public double area() {
        return Math.PI * raggio * raggio;
    }
}
```

---
### INTERFACCE
**Interfacce** in Java sono un tipo di classe astratta pura che definisce solo i metodi senza implementazione. Le classi che “implementano” un’interfaccia devono fornire il codice concreto per tutti i metodi dichiarati. Le interfacce permettono di definire contratti comuni che classi diverse possono rispettare, facilitando la programmazione orientata ai servizi e l’uso del polimorfismo.

```java
public interface Volante {
    void vola();
}

public class Uccello implements Volante {
    @Override
    public void vola() {
        System.out.println("Sto volando!");
    }
}
```