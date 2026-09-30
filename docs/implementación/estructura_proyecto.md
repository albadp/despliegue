# Estructura del proyecto

La aplicación se organiza de la siguiente forma:

```text
taskflow/
├── docs/
│   ├── intro.md
│   ├── arquitectura.md
│   ├── análisis/
│   │   └── requisitos.md
│   ├── diseño/
│   │   └── diagrama_clases.md
│   ├── implementación/
│   │   └── estructura_proyecto.md
│   ├── pruebas/
│   │   └── analisis_caja_blanca.md
│   └── despliegue/
│       └── github_pages.md
│
├── src/
│   ├── models/
│   │   ├── Tarea.js
│   │   ├── Proyecto.js
│   │   └── Usuario.js
│   │
│   ├── services/
│   │   ├── TareaService.js
│   │   └── ProyectoService.js
│   │
│   ├── components/
│   │   ├── TaskList.js
│   │   ├── TaskForm.js
│   │   └── ProjectList.js
│   │
│   ├── storage/
│   │   └── LocalStorageRepository.js
│   │
│   └── main.js
│
├── tests/
│   ├── Tarea.test.js
│   └── Proyecto.test.js
│
├── index.html
├── package.json
└── README.md
```

## Descripción de directorios

### `models/`

Contiene las entidades principales del dominio.

### `services/`

Contiene la lógica de negocio y las operaciones sobre las entidades.

### `components/`

Contiene los componentes encargados de la interfaz.

### `storage/`

Gestiona el almacenamiento y recuperación de información.

### `tests/`

Contiene las pruebas automatizadas.

---

