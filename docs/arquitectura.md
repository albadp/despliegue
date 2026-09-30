# Arquitectura del sistema

TaskFlow utiliza una arquitectura dividida en tres capas principales:

```text
┌─────────────────────────────┐
│       Interfaz de usuario   │
│          (UI / Web)         │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│       Lógica de negocio     │
│       Servicios / Modelos   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│       Persistencia          │
│      LocalStorage API       │
└─────────────────────────────┘
```

## Capa de presentación

Es responsable de mostrar la información al usuario y capturar sus acciones.

Entre sus componentes se encuentran:

- Lista de proyectos.
- Lista de tareas.
- Formularios.
- Filtros.
- Panel de información.

## Capa de lógica de negocio

Contiene las reglas principales de la aplicación.

Ejemplos:

- Una tarea debe pertenecer a un proyecto.
- Una tarea puede tener uno de varios estados definidos.
- Una tarea completada no puede volver automáticamente a estado pendiente.
- Las fechas de vencimiento deben tener un formato válido.

## Capa de persistencia

La primera versión utiliza `LocalStorage` para almacenar la información.

Esto permite que la aplicación funcione sin un servidor backend.

---

