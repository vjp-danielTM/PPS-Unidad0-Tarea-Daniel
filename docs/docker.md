# Introducción
Este documento muestra el despliegue mediante Docker de la documentación estática de la pagina principal mia, servida con Nginx en el puerto 8085.

---

## Fase 1: Preparación del Entorno

## Ejecución del contenedor Docker
![docker run](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/1docker.png)

Comando ejecutado para levantar el contenedor:

> docker run -d \
  --name PPSUnidad0-Tarea-daniel_trujillo \
  -p 8085:80 \
  -v "$(pwd)":/usr/share/nginx/html:ro \
  nginx:alpine


```docker run```

Crea un nuevo contenedor desde una imagen y lo inicia automáticamente-dEjecuta el contenedor en segundo plano (no bloquea tu terminal)

```--name PPSUnidad0-Tarea-daniel_trujillo```

Le pone ese nombre exacto al contenedor para poder usarlo después

```-p 8085:80```

Conecta el puerto 8085 de tu máquina con el puerto 80 del contenedor → tú entras por localhost:8085

```-v "$(pwd)":/usr/share/nginx/html:ro```

Monta la carpeta donde estás ahora mismo dentro del contenedor en la ruta donde Nginx busca las páginas web, y en modo solo lectura (:ro)

```nginx:alpine```

Usa la imagen oficial de Nginx basada en Alpine Linux Alpine (la más pequeña y ligera)


```docker ps ```

Verifica los contenedores que hay activo


## Fase 2: Acceso a la Documentación Web
Resultado en el navegador

[Aqui se veria desde mi maquina la pagina de nginx](http://localhost:8085)

![docker run](https://raw.githubusercontent.com/vjp-danielTM/PPS-Unidad0-Tarea-Daniel/refs/heads/main/docs/imagen/2docker.png)

## Conclusiones Finales

1. **Portabilidad total del entorno:**  
   Gracias a Docker, la documentación y la aplicación se ejecutan exactamente igual en cualquier máquina (Kali, Ubuntu, Windows, macOS) sin instalar nada extra, solo con tener Docker instalado.

2. **Aislamiento y seguridad:**  
   El contenedor nginx:alpine funciona completamente aislado del sistema host, evita conflictos de dependencias y reduce la superficie de ataque al usar una imagen mínima y en modo solo lectura.

3. **Despliegue instantáneo de sitios estáticos:**  
   Con un solo comando y un volumen montado, cualquier carpeta con archivos HTML se convierte inmediatamente en un servidor web profesional accesible desde el navegador.

4. **Reproducibilidad perfecta:**  
   Cualquier compañero o profesor puede replicar exactamente el mismo entorno con el mismo comando `docker run`, garantizando que todos vean lo mismo que tú.

5. **Aprendizaje práctico de contenedores:**  
   Este ejercicio demuestra de forma clara y sencilla los conceptos clave de Docker: imágenes, contenedores, puertos, volúmenes y ejecución en segundo plano, todo aplicado a un caso real de entrega de una tarea.
