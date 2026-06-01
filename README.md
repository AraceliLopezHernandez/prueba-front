# prueba-front

Proyecto frontend base con una pagina HTML inicial que utiliza Bootstrap 5 por CDN.

## Contenido

- `index.html`: pagina estatica con navbar en Bootstrap.
- `.github/workflows/ci.yml`: validaciones basicas para PR y pushes a `dev`, `qa` y `main`.
- `.github/workflows/deploy-pages.yml`: despliegue automatico a GitHub Pages desde `main`.

## Tecnologias

- HTML5
- Bootstrap 5

## Como usar

1. Clona este repositorio.
2. Abre `index.html` en tu navegador.

## Flujo CI/CD

`dev` es la rama de desarrollo.

`qa` es la rama de validacion.

`main` es la rama productiva.

El deploy a GitHub Pages solo ocurre desde `main`.

Los nombres de ramas, commits y Pull Requests deben incluir la key de Jira, por ejemplo `CP-1`.

```text
Jira task
  ↓
Crear rama desde Jira: CP-1-Agregar-navbar
  ↓
Pull Request: CP-1-Agregar-navbar -> dev
  ↓
Merge a dev
  ↓
Pull Request: dev -> qa
  ↓
Merge a qa
  ↓
Pull Request: qa -> main
  ↓
Merge a main
  ↓
Deploy automatico a GitHub Pages
```

## Estructura

```text
prueba-front/
|-- .github/
|   `-- workflows/
|       |-- ci.yml
|       `-- deploy-pages.yml
|-- index.html
|-- README.md
`-- .gitignore
```
