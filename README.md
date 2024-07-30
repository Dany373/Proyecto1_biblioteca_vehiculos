# Biblioteca De Vehiculos

## Clase ‘Vehiculo.java’

```java
package biblioteca_vehiculos;
public class Vehiculo {
    private String marca;
    private String modelo;
    private int anio;

    public Vehiculo(String marca, String modelo, int anio) {
        this.marca = marca;
        this.modelo = modelo;
        this.anio = anio;
    }

    // Metodos getter y setter

    public String getMarca() {
        return marca;
    }
    public void setMarca(String marca) {
        this.marca = marca;
    }
    public String getModelo() {
        return modelo;
    }
    public void setModelo(String modelo) {
        this.modelo = modelo;
    }
    public int getAnio() {
        return anio;
    }
    public void setAnio(int anio) {
        this.anio = anio;
    }

    public void mostrarDetalles(){
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Anio: " + anio);
    }

    @Override
    public String toString() {
        return "Vehiculo{" + "marca=‘" + marca + ", modelo=" + modelo + ", anio=" + anio + '}';

    }
} 



 Clase Coche.java

package biblioteca_vehiculos;

public class Coche extends Vehiculo {
    private int numeroDePuertas;
    public Coche(String marca, String modelo,int anio, int numeroDePuertas) {
        super(marca,modelo,anio);
        this.numeroDePuertas = numeroDePuertas;
    }
    public int getNumeroDePuertas() {
        return numeroDePuertas;
    }
    public void setNumeroDePuertas(int numeroDePuertas) {
        this.numeroDePuertas = numeroDePuertas;
    }
    @Override
    public void mostrarDetalles(){
        super.mostrarDetalles();
        System.out.println("Numero de puertas: " + numeroDePuertas);
    }
}


 Clase Moto.java

package biblioteca_vehiculos;

public class Moto extends Vehiculo {

    private boolean tieneSidecar;
    public Moto(String marca, String modelo, int anio, boolean tieneSidecar) {
        super(marca, modelo, anio);
        this.tieneSidecar = tieneSidecar;
    }
    public boolean isTieneSidecar() {
        return tieneSidecar;
    }
    public void setTieneSidecar(boolean tieneSidecar) {
        this.tieneSidecar = tieneSidecar;
    }

    @Override
    public void mostrarDetalles(){
        super.mostrarDetalles();
        System.out.println("Tiene Sidecar: " + (tieneSidecar ? "Sí" : "No"));
    }
}
