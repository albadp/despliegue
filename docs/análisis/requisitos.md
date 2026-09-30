# Análisis de requisitos

## Requisitos funcionales

### RF-01. Crear proyecto

El usuario podrá crear un proyecto indicando:

- Nombre.
- Descripción.
- Fecha de creación.

### RF-02. Crear tarea

El usuario podrá crear una tarea asociada a un proyecto.

La tarea tendrá:

- Identificador.
- Título.
- Descripción.
- Estado.
- Prioridad.
- Fecha de vencimiento.
- Usuario responsable.

### RF-03. Modificar tarea

El usuario podrá modificar los datos de una tarea existente.

### RF-04. Eliminar tarea

El usuario podrá eliminar una tarea después de confirmar la operación.

### RF-05. Filtrar tareas

El sistema permitirá filtrar las tareas por:

- Estado.
- Prioridad.
- Responsable.
- Proyecto.

### RF-06. Completar tarea

El usuario podrá cambiar el estado de una tarea a `COMPLETADA`.

## Requisitos no funcionales

### RNF-01. Usabilidad

La interfaz deberá ser comprensible para un usuario sin conocimientos técnicos.

### RNF-02. Rendimiento

Las operaciones habituales deberán completarse en menos de un segundo en un navegador moderno.

### RNF-03. Compatibilidad

La aplicación deberá funcionar en las versiones recientes de Chrome, Firefox, Edge y Safari.

### RNF-04. Mantenibilidad

El código deberá estar organizado por responsabilidades y evitar dependencias innecesarias entre componentes.

---
