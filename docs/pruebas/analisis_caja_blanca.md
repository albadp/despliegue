# Análisis de caja blanca

El análisis de caja blanca se utiliza para estudiar la estructura interna del código y comprobar que las diferentes rutas de ejecución han sido probadas.

## Función analizada

Se analiza la función ficticia `completarTarea()`:

```javascript
function completarTarea(tarea) {
    if (!tarea) {
        return false;
    }

    if (tarea.estado === "COMPLETADA") {
        return false;
    }

    tarea.estado = "COMPLETADA";
    return true;
}
```

## Grafo de control

La función contiene tres decisiones principales:

```text
Inicio
  |
  v
¿Existe tarea?
  |
  +---- NO ----> false
  |
  SI
  |
  v
¿Está completada?
  |
  +---- SI ----> false
  |
  NO
  |
  v
Cambiar estado
  |
  v
 true
```

## Complejidad ciclomática

La complejidad ciclomática puede calcularse mediante:

```text
M = decisiones + 1
```

La función contiene dos decisiones:

```text
M = 2 + 1
M = 3
```

Por tanto, se necesitan como mínimo tres caminos independientes para cubrir la estructura de decisión.

## Casos de prueba

| Caso | Entrada | Resultado esperado |
|---|---|---|
| CP-01 | `null` | `false` |
| CP-02 | Tarea ya completada | `false` |
| CP-03 | Tarea pendiente | `true` |

## Conclusión

Los tres casos permiten recorrer las principales rutas independientes de la función analizada y comprobar tanto las condiciones de error como el camino normal de ejecución.

---
