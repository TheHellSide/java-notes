### INCAPSULAMENTO
**Incapsulamento** è il principio di nascondere i dettagli interni di un oggetto e di proteggere i dati. Significa che gli attributi di una classe sono generalmente dichiarati privati e possono essere modificati o letti solo tramite metodi pubblici detti getter e setter. Questo permette di controllare l’accesso ai dati, migliorare la sicurezza e mantenere l’integrità dello stato dell’oggetto.

```java
public class Persona {
    private String nome;  // attributo privato
	
    public String getNome() {
        return nome;      // getter per leggere il nome
    }
	
    public void setNome(String nome) {
        this.nome = nome; // setter per modificare il nome
    }
}
```