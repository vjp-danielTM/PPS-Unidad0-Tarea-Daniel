# Introducción
Este documento describe el proceso completo de configuración y despliegue de un proyecto utilizando Git, GitHub Actions y documentación con MkDocs.  
El proyecto consiste en una calculadora en Python con documentación automatizada.

---

## Fase 1: Preparación del Entorno

## Configuración de Archivos del Proyecto
![imagen1](docs/imagen/1git.png)

En esta fase inicial, se organizan los archivos necesarios para el proyecto:


### Copiar archivos de configuración desde otro proyecto para tener lo que tenia en DevSecOps
```cp -r calculator/docs/mkdocs.yml requirements.txt .github/.../ ```

### Moverse al directorio anterior para tener visión general
```cd ...```

### Listar contenido para verificar estructura
ls

### Mover archivos esenciales al proyecto actual
```mv calculator/docs/mkdocs.yml requirements.txt .github/ PPS-Unidad0-Tarea-Daniel/```

### Verificar la transferencia exitosa
```cd PPS-Unidad0-Tarea-Daniel/ ```

``` ls ```
## Fase 2: Creación de Documentación

#### Estructura de Archivos de Documentación
![imagen2](/docs/imagen/2git.png)

Se crea la estructura completa de documentación técnica:


### Acceder al directorio de documentación
```cd docs/```

### Crear archivos de documentación específicos
```touch git.md gitActions.md gitPages.md docker.md ```
```conclusions.md ```

### Verificar estructura creada
```tree```

### Regresar y ver estructura completa del proyecto
```cd ..```

```tree```
## Fase 3: Commit y Despliegue

### Subida del Proyecto a GitHub
![imagen3](/docs/imagen/3git.png)

Una vez configurado todo el proyecto, se procede al commit y push:


### Agregar todos los cambios al staging area
```git add .```

### Crear commit con mensaje descriptivo
```git commit -am "Ejercicio de git obligatorio"```

### Subir cambios al repositorio remoto
```git push origin main```
## Fase 4: Verificación Final

### Estado del Repositorio
![imagen4](/docs/imagen/4git.png)

Se verifica la estructura y el estado del repositorio en GitHub:

### Comprobar rama principal
```git branch```

### Verificar último commit
```git log -1```

### Listar carpetas y archivos en la rama principal
```ls -R```
## Conclusiones Finales

1. **Automatización del flujo de trabajo:**  
   La integración de GitHub Actions permite automatizar la construcción y despliegue de la documentación, lo que asegura que cualquier cambio en el proyecto se vea reflejado de manera inmediata en la documentación pública.

2. **Organización y claridad del proyecto:**  
   Mantener una estructura clara de archivos y carpetas (código fuente, documentación, configuraciones) facilita el mantenimiento, la colaboración y la escalabilidad del proyecto.

3. **Buenas prácticas de control de versiones:**  
   El uso de Git para commits frecuentes y descriptivos garantiza trazabilidad de cambios y facilita la identificación de errores o mejoras en el proyecto.

4. **Documentación accesible:**  
   La combinación de MkDocs y GitHub Pages permite generar una documentación profesional, navegable y actualizada automáticamente, mejorando la comunicación del proyecto a cualquier colaborador o usuario final.

5. **Aprendizaje integral:**  
   Este proyecto combina programación en Python, control de versiones, integración continua y generación de documentación automatizada, proporcionando una experiencia completa de desarrollo profesional.
