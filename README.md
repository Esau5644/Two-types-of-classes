# ¡Hola! Soy Esau 👋

Bienvenido a mi perfil de GitHub. Soy un estudiante del CETis 17 con un poco de conocimiento sobre lenguajes de programación. En este README, te mostraré cómo crear y conectar dos clases en Java.

## Proyecto: Conexión de Clases en Java

En este proyecto, he creado dos clases en Java: `Persona` y `Estudiante`. La clase `Estudiante` extiende de `Persona`, demostrando la herencia en Java.

### Clase Persona

La clase `Persona` contiene los atributos `nombre` y `edad`, junto con un constructor, getters y un método para mostrar la información.

```java
public class Persona {
    private String nombre;
    private int edad;

    // Constructor
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Getters
    public String getNombre() {
        return nombre;
    }

    public int getEdad() {
        return edad;
    }

    // Método para mostrar información
    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }
}
public class Estudiante extends Persona {
    private String escuela;

    // Constructor
    public Estudiante(String nombre, int edad, String escuela) {
        super(nombre, edad);
        this.escuela = escuela;
    }

    // Getter
    public String getEscuela() {
        return escuela;
    }

    // Método para mostrar información específica de Estudiante
    @Override
    public void mostrarInformacion() {
        super.mostrarInformacion();
        System.out.println("Escuela: " + escuela);
    }
}
public static void main(String[] args) {
    // Crear instancia de Persona
    Persona persona = new Persona("Carlos", 30);
    persona.mostrarInformacion();

    // Crear instancia de Estudiante
    Estudiante estudiante = new Estudiante("Esau", 18, "CETis 17");
    estudiante.mostrarInformacion();
}

