# Despliegue mediante GitHub Pages

GitHub Pages permite publicar la versión estática de TaskFlow directamente desde un repositorio de GitHub.

## Requisitos previos

Es necesario disponer de:

- Una cuenta de GitHub.
- Un repositorio para el proyecto.
- El código fuente de TaskFlow.
- Un archivo `index.html`.

## Configuración

El proyecto se subirá al repositorio mediante:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/usuario/taskflow.git
git push -u origin main
```

Posteriormente se accederá a la configuración del repositorio y se habilitará GitHub Pages.

La fuente de publicación será la rama:

```text
main
```

y el directorio:

```text
/
```

## Proceso de publicación

El flujo de despliegue será:

```text
Desarrollador
     |
     v
Git commit
     |
     v
GitHub
     |
     v
GitHub Pages
     |
     v
Aplicación publicada
```

## URL ficticia

Una vez publicado, el proyecto podría estar disponible en:

```text
https://usuario.github.io/taskflow/
```

## Consideraciones

GitHub Pages es apropiado para esta versión porque TaskFlow no necesita un servidor backend.

Si en futuras versiones se incorporasen autenticación, una base de datos remota o una API privada, sería necesario complementar GitHub Pages con una infraestructura backend.

---
