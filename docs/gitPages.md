# GH-PAGES
## Objetivo conseguido
Guía completa para configurar y desplegar la documentación en GitHub Pages, haciendo que sea accesible públicamente en internet.

## Pasos realizados (con evidencias)

### 1. Configuración de GitHub Pages
Entré en Settings → Pages y configuré el despliegue desde la rama gh-pages.

![Configuración de GitHub Pages – rama gh-pages seleccionada](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/1workflo)

### 2. Creación y prueba del workflow en GitHub Actions
Creé el archivo `.github/workflows/deploy-mkdocs.yml`.  
Cada push a main ejecuta automáticamente el workflow “Deploy MkDocs”.

![Se ve el workflow creado y ejecutado correctamente](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/3workflo)


### 3. Resultado final: sitio web publicado
La documentación ya está publicada y accesible públicamente en GitHub Pages.

![Sitio web de documentación generado con MkDocs](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/4workflo)


### 4. Contenido de la documentación publicada
- Título: Calculadora Python  
- Descripción del proyecto  
- Instrucciones de uso: ejecutar `calculator/gui.py`  
- Requisitos: Python 3.x + Tkinter  


## Workflow paso a paso (lo que hace GitHub Actions)

![Logs detallados del workflow](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/2workflo)





---