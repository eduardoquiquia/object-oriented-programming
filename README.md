
# 🧱 Programación Orientada a Objetos (POO)

La **Programación Orientada a Objetos (POO)** es un paradigma de programación basado en la idea de "objetos", que son entidades que combinan **datos** (atributos) y **comportamientos** (métodos). Este enfoque permite modelar el software de forma similar a como entendemos el mundo real: a través de entidades con características y comportamientos propios.

---

## 🎯 Principales conceptos de POO

### 1. 🛠️ _Constructores_

Un **constructor** es un método especial que se ejecuta cuando se crea un objeto. Se usa para inicializar los atributos del objeto.

### 🧪 Ejemplo:
```Java
public class Persona {
    private String nombre;

    public Persona(String nombre) {
        this.nombre = nombre;
    }
}
```

### 2. 🧱 Modificadores de acceso

Los **modificadores de acceso** controlan la visibilidad de clases, atributos y métodos. En Java, los principales son:

| Modificador | Accesible desde... |
|-------------|--------------------|
| ```public``` | Cualquier clase |
| ```private``` | Solo dentro de la misma clase |
| ```protected``` | Mismo paquete o subclases |
| (sin nada) | Solo dentro del mismo paquete |
 

### 3. 🔍 _Abstracción_

La **abstracción** es el proceso de ocultar los detalles complejos de un sistema y mostrar solo lo necesario. Permite centrarse en **"qué hace"** un objeto en lugar de **"cómo lo hace"**.

### 🧪 Ejemplo:
```Java
public abstract class Animal {
    public abstract void hacerSonido();
}
```

### 4. 🔐 _Encapsulamiento_

El **encapsulamiento** consiste en ocultar los datos internos de un objeto y permitir el acceso a ellos solo a través de métodos públicos (getters y setters). Esto protege los datos y reduce el acoplamiento.

✅ Se logra usando modificadores de acceso (como private, public, protected) y métodos getters y setters.

### 🧪 Ejemplo:

```Java
public class Persona {
    private String nombre;

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

### 5. 🧬 _Herencia_

La **herencia** permite que una clase (subclase) herede atributos y métodos de otra clase (superclase), facilitando la reutilización de código.

### 🧪 Ejemplo:

```Java
public class Animal {
    public void comer() {
        System.out.println("El animal come.");
    }
}

public class Perro extends Animal {
    public void ladrar() {
        System.out.println("El perro ladra.");
    }
}

Animal miMascota = new Perro();
miMascota.comer();
```

### 6. 🌀 _Polimorfismo_

El **polimorfismo** permite que una misma operación se comporte de manera diferente según el objeto que la implemente. Hay dos tipos: sobreescritura (override) y sobrecarga (overload).

### 🧪 Ejemplo:

```Java
public class Animal {
    public void hacerSonido() {
        System.out.println("Sonido genérico");
    }
}

public class Gato extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Miau");
    }
}
```

### 7. 📚 _Interfaces y Colecciones_

En Java, las interfaces como ```List```, ```Set``` y ```Map ``` definen estructuras de datos comunes. Cada una tiene implementaciones concretas con comportamientos específicos:

### 7.1 🔁 List

Una colección ordenada que permite elementos duplicados.
**Implementaciones comunes:**

- ```ArrayList``` → rápido para acceder

- ```LinkedList``` → mejor para inserciones/remociones frecuentes

### 🧪 Ejemplo:

```Java
List<String> nombres = new ArrayList<>();
nombres.add("Ana");
nombres.add("Luis");
```

### 7.2 ✅ Set

Una colección **no ordenada** que **no permite duplicados**.

**Implementaciones comunes:**

- ```HashSet``` → rápido, no garantiza orden

- ```TreeSet``` → mantiene orden natural

- ```LinkedHashSet``` → mantiene el orden de inserción

### 🧪 Ejemplo:

```Java
Set<String> frutas = new HashSet<>();
frutas.add("Manzana");
frutas.add("Banana");
```

### 7.3 🗺️ Map

Una estructura que almacena pares **clave-valor**.

**Implementaciones comunes:**

- ```HashMap``` → no garantiza orden

- ```TreeMap``` → ordenado por clave

- ```LinkedHashMap``` → mantiene orden de inserción

### 🧪 Ejemplo:

```Java
Map<Integer, String> mapa = new HashMap<>();
mapa.put(1, "Uno");
mapa.put(2, "Dos");
```

### 📅 Última actualización: 16 Abril 2025



