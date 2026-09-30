# Diagrama de clases

El modelo conceptual de TaskFlow está compuesto principalmente por las clases `Usuario`, `Proyecto` y `Tarea`.

```mermaid
classDiagram

class Usuario {
    +String id
    +String nombre
    +String email
}

class Proyecto {
    +String id
    +String nombre
    +String descripcion
    +Date fechaCreacion
    +agregarTarea()
    +eliminarTarea()
}

class Tarea {
    +String id
    +String titulo
    +String descripcion
    +EstadoTarea estado
    +Prioridad prioridad
    +Date fechaVencimiento
    +completar()
    +actualizar()
}

class EstadoTarea {
    <<enumeration>>
    PENDIENTE
    EN_PROGRESO
    COMPLETADA
}

class Prioridad {
    <<enumeration>>
    BAJA
    MEDIA
    ALTA
}

Usuario "1" --> "0..*" Tarea : responsable
Proyecto "1" --> "0..*" Tarea : contiene
Tarea --> EstadoTarea
Tarea --> Prioridad
```

## Relaciones

Un usuario puede ser responsable de varias tareas.

Un proyecto puede contener ninguna o varias tareas.

Cada tarea pertenece obligatoriamente a un único proyecto.

El estado y la prioridad de una tarea se representan mediante enumeraciones para limitar los valores posibles.

---
