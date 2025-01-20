# Contenedor de Docker para el Curso de Monte Carlo

Bienvenidos al Curso de Monte Carlo. Este documento te guiará a través de la configuración y el uso de un entorno Docker optimizado para el desarrollo y ejecución de proyectos relacionados con Monte Carlo. A continuación, encontrarás una introducción a Docker, instrucciones detalladas sobre cómo utilizarlo, y una lista completa de comandos útiles para gestionar tu entorno Docker de manera eficiente.

## Introducción a Docker

Antes de sumergirnos en los conceptos y aplicaciones avanzadas de Monte Carlo, es fundamental comprender las herramientas que facilitarán nuestro aprendizaje y desarrollo durante el curso. Una de estas herramientas clave es **Docker**. En esta sección, exploraremos qué es Docker, cómo se utiliza y los beneficios que aporta específicamente a nuestro curso.

### ¿Qué es Docker?

**Docker** es una plataforma de código abierto que permite automatizar la creación, despliegue y gestión de contenedores de software. Un contenedor es una unidad estándar de software que empaqueta el código de una aplicación junto con todas sus dependencias, bibliotecas y configuraciones necesarias para que funcione de manera consistente en cualquier entorno.

**Componentes Clave de Docker:**

- **Imagen (Image)**: Una plantilla inmutable que contiene el sistema de archivos y las configuraciones necesarias para ejecutar una aplicación.
- **Contenedor (Container)**: Una instancia en ejecución de una imagen. Los contenedores son aislados y portátiles.
- **Dockerfile**: Un archivo de texto que contiene una serie de instrucciones para construir una imagen de Docker.
- **Docker Compose**: Una herramienta que permite definir y gestionar aplicaciones multi-contenedor utilizando un archivo YAML.

### ¿Cómo se Usa Docker?

Docker se utiliza para crear entornos de desarrollo y producción que sean consistentes y reproducibles. A continuación, se describen algunos usos comunes de Docker:

1. **Desarrollo de Aplicaciones**: Los desarrolladores pueden crear contenedores que replican el entorno de producción, asegurando que el código funcione de la misma manera en diferentes máquinas.
2. **Pruebas y QA**: Facilita la creación de entornos aislados para realizar pruebas automatizadas y garantizar la calidad del software.
3. **Despliegue de Aplicaciones**: Permite desplegar aplicaciones de manera rápida y eficiente en diferentes plataformas y servicios en la nube.
4. **Microservicios**: Docker es ideal para arquitecturas basadas en microservicios, donde cada componente de la aplicación se ejecuta en su propio contenedor.

**Flujo de Trabajo Básico con Docker:**

1. **Escribir un Dockerfile**: Define las instrucciones para construir la imagen de Docker.
2. **Construir la Imagen**: Utiliza el comando `docker build` para crear una imagen a partir del Dockerfile.
3. **Ejecutar un Contenedor**: Inicia un contenedor basado en la imagen creada.
4. **Gestionar Contenedores**: Utiliza comandos como `docker ps`, `docker stop`, y `docker rm` para gestionar los contenedores en ejecución.

### Beneficios de Usar Docker en Este Curso

Integrar Docker en nuestro curso de Monte Carlo ofrece múltiples ventajas que enriquecerán tu experiencia de aprendizaje:

1. **Entorno Consistente**: Docker garantiza que todos los estudiantes trabajen en el mismo entorno de desarrollo, eliminando las discrepancias que pueden surgir debido a diferencias en las configuraciones locales. Esto asegura que el código y las aplicaciones funcionen de manera idéntica para todos.

2. **Fácil Configuración y Despliegue**: Con Docker, configurar el entorno de desarrollo es rápido y sencillo. No necesitas preocuparte por instalar manualmente dependencias, bibliotecas o herramientas específicas. Simplemente clonas el repositorio, construyes el contenedor y estás listo para comenzar.

3. **Aislamiento de Proyectos**: Cada proyecto o ejercicio puede ejecutarse en su propio contenedor aislado, evitando conflictos entre diferentes versiones de software o dependencias. Esto facilita la gestión de múltiples proyectos simultáneamente.

4. **Portabilidad**: Los contenedores Docker pueden ejecutarse en cualquier sistema que soporte Docker, ya sea tu computadora local, un servidor remoto o en la nube. Esto permite que puedas continuar tu trabajo desde diferentes ubicaciones sin problemas de compatibilidad.

5. **Reproducibilidad**: Docker facilita la replicación de entornos y experimentos, lo cual es crucial en metodologías como Monte Carlo donde la reproducibilidad de resultados es fundamental. Puedes compartir fácilmente tu entorno con otros estudiantes o colaboradores, asegurando que todos trabajen bajo las mismas condiciones.

6. **Escalabilidad**: A medida que avances en el curso y trabajes en proyectos más complejos, Docker te permitirá escalar tu entorno de desarrollo sin dificultades, gestionando recursos de manera eficiente y optimizando el rendimiento.

7. **Aprendizaje de Herramientas Industriales**: Docker es una herramienta ampliamente utilizada en la industria del software y la ciencia de datos. Al familiarizarte con Docker durante este curso, adquirirás habilidades valiosas que serán altamente apreciadas en el mercado laboral.

### Conclusión

Docker es una herramienta poderosa que transformará la manera en que desarrollas y gestionas tus proyectos en el Curso de Monte Carlo. Al aprovechar sus capacidades, podrás enfocarte en los conceptos y técnicas de Monte Carlo sin preocuparte por las complicaciones técnicas relacionadas con el entorno de desarrollo. En las próximas secciones, profundizaremos en la configuración del entorno y en el uso práctico de Docker, aprendiendo a construir, gestionar y optimizar contenedores para maximizar tu productividad y eficiencia.

---

## Instrucciones para Configurar el Entorno

Este proyecto permite configurar y ejecutar un entorno Docker con JupyterLab de forma rápida. Sigue estos pasos para asegurarte de que todo funcione correctamente.

### Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

1. **Windows Terminal**: Necesario para ejecutar comandos en la terminal.
2. **Git**: Necesario para clonar el repositorio.
3. **Docker Desktop**: Necesario para ejecutar contenedores Docker.

### Instalación Paso a Paso

#### 1. Clonar el Repositorio

Ve al Escritorio, haz clic derecho y selecciona **Abrir en Windows Terminal**. Clona el repositorio con el siguiente comando:
```bash
git clone https://github.com/guillermoibarra/mc-docker-env.git
```
#### 2. Construir el Contenedor

Navega al directorio raíz del proyecto recién clonado:
```bash
cd mc-docker-env
```

Construir el contenedor:
```bash
docker-compose build
```

Iniciar el contenedor en modo despejado:
```bash
docker-compose up -d
```

Verificar el contenedor:
```bash
docker ps
```

#### 3. Ejecutar el Contenedor
Empezar el proceso `zsh`:
```bash
docker exec -it mc-taller-env-container zsh
```

---

## Comandos Adicionales Útiles para Docker

Además de los comandos básicos que ya has incluido en el README, hay una serie de comandos adicionales que pueden ser muy útiles para gestionar y mantener tu entorno Docker durante el curso de Monte Carlo. A continuación, se presentan estos comandos junto con una breve explicación de su uso y ejemplos prácticos en el contexto de nuestro proyecto.

### 1. Detener los Contenedores

Para detener los contenedores que están actualmente en ejecución, puedes usar:
```bash
docker-compose down
```

Este comando detiene y elimina los contenedores, redes y volúmenes definidos en el archivo `docker-compose.yml`. Es útil cuando necesitas reiniciar el entorno o liberar recursos del sistema.

### 2. Reiniciar los contenedores

Si necesitas reiniciar los contenedores después de realizar cambios en la configuración o en el código, puedes usar:
```bash
docker-compose restart
```

Reinicia todos los contenedores definidos en el archivo `docker-compose.yml` sin reconstruir las imágenes.

### 3. Ver los Logs de un Contenedor

Para diagnosticar problemas o simplemente monitorear lo que está sucediendo dentro de un contenedor, puedes ver sus logs:
```bash
docker logs <nombre_del_contenedor>
```

Muestra los registros de salida del contenedor especificado, lo que es útil para depuración y monitoreo.

### 4. Actualizar el Entorno Después de Cambios

Si realizas cambios en el `Dockerfile` o en el `docker-compose.yml`, necesitarás reconstruir las imágenes y reiniciar los contenedores:
```bash
docker-compose up -d --build
```

Este comando reconstruye las imágenes según las modificaciones realizadas y luego inicia los contenedores en modo desacoplado.

### 5. Eliminar Imágenes No Utilizadas

Para mantener tu sistema limpio y liberar espacio, puedes eliminar imágenes que ya no se utilizan:
```bash
docker image prune
```

Elimina todas las imágenes que no están siendo utilizadas por ningún contenedor.

### 6. Acceder a la Terminal del Contenedor con Bash

Aunque estamos usando `zsh`, a veces puede ser útil acceder al contenedor usando bash si está disponible:
```bash
docker exec -it mc-taller-env-container zsh
```

### 7. Listar Todos los Contenedores (Activos e Inactivos)

Para ver todos los contenedores, incluyendo los que no están en ejecución:
```bash
docker ps -a
```

Muestra una lista completa de todos los contenedores, proporcionando información sobre su estado actual.

### 8. Eliminar un Contenedor Específico

Si necesitas eliminar un contenedor específico, primero asegúrate de que esté detenido y luego elimínalo:
```bash
docker rm <nombre_del_contenedor>
```

Elimina el contenedor especificado de tu sistema. Útil para limpiar contenedores que ya no necesitas.

### 9. Ver las Imágenes Disponibles en tu Sistema
Para listar todas las imágenes de Docker que tienes localmente:
```bash
docker images
```

Muestra una lista de todas las imágenes descargadas en tu sistema, incluyendo sus etiquetas y tamaños.

### 10. Inspeccionar un Contenedor o Imagen

Para obtener detalles detallados sobre un contenedor o una imagen específica:
```bash
docker inspect <nombre_del_contenedor_o_imagen>
```

Proporciona información detallada en formato JSON sobre la configuración y el estado del contenedor o la imagen.

### 11. Comprobar el Estado del Sistema Docker

Para obtener una visión general del estado actual de Docker en tu sistema:
```bash
docker system info
```

Muestra información detallada sobre la configuración de Docker, incluyendo versiones, recursos utilizados y más.

### 12. Limpiar Recursos No Utilizados

Para liberar espacio eliminando contenedores detenidos, imágenes no utilizadas, volúmenes sin referencia y redes no utilizadas:
```bash
docker system prune
```

Ejecuta una limpieza completa eliminando todos los recursos no utilizados, ayudando a mantener tu sistema optimizado.

### 13. Ejecutar Comandos en un Contenedor en Ejecución

Para ejecutar cualquier comando adicional dentro de un contenedor en ejecución:
```bash
docker exec -it <nombre_del_contenedor> <comando>
```

### 14. Guardar y Cargar Imágenes de Docker
Guardar una Imagen:
```bash
docker save -o <archivo_de_salida>.tar <nombre_de_la_imagen>
```

Exporta una imagen de Docker a un archivo tar, facilitando su distribución o respaldo.

Cargar una Imagen:
```bash
docker load -i <archivo_de_entrada>.tar
```

Importa una imagen de Docker desde un archivo tar previamente guardado.

### 15. Buscar Imágenes en Docker Hub

Para buscar imágenes disponibles en Docker Hub directamente desde la terminal:
```bash
docker search <término_de_búsqueda>
```

Ayuda a encontrar imágenes oficiales o de terceros que puedan ser útiles para tu proyecto.

### 16. Actualizar Docker Compose

Mantener `docker-compose` actualizado es crucial para aprovechar las últimas mejoras y correcciones de errores. Para actualizar `docker-compose` en sistemas basados en Unix:
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/<versión>/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

Reemplaza `<versión>` con la versión deseada para descargar e instalar la última versión de `docker-compose`.

### 17. Mover Archivos hacia y desde el Contenedor

Para mover archivos entre tu sistema host y el contenedor Docker, puedes utilizar el comando `docker cp`. En nuestro entorno, hemos definido un volumen:
```yaml
volumes:
      - taller_data:/home/taller
```

Esto significa que el directorio `/home/taller` dentro del contenedor está asociado al volumen `taller_data`. Aunque los volúmenes nombrados no son fácilmente accesibles directamente desde el host, `docker cp` es una herramienta eficaz para transferir archivos.

Para copiar un archivo o directorio desde tu sistema host al contenedor, usa el siguiente comando:
```bash
docker cp <ruta_en_host> mc-taller-env-container:/home/taller/
```

Por ejemplo, supongamos que tienes un archivo llamado data.csv en tu escritorio y deseas copiarlo al directorio `/home/taller` dentro del contenedor:
```bash
docker cp ~/Desktop/data.csv mc-taller-env-container:/home/taller/
```

Para copiar un archivo o directorio desde el contenedor a tu sistema host, usa:
```bash
docker cp mc-taller-env-container:/home/taller/<archivo_o_directorio> <ruta_en_host>
```

## Resumen de Comandos Clave

| Comando                                         | Descripción                                           |
|-------------------------------------------------|-------------------------------------------------------|
| `docker-compose down`                           | Detiene y elimina contenedores, redes y volúmenes.    |
| `docker-compose restart`                        | Reinicia los contenedores sin reconstruir imágenes.   |
| `docker logs <contenedor>`                      | Muestra los logs de un contenedor específico.         |
| `docker-compose up -d --build`                  | Reconstruye imágenes y reinicia los contenedores.     |
| `docker image prune`                            | Elimina imágenes no utilizadas.                       |
| `docker exec -it <contenedor> bash`             | Accede al contenedor usando bash.                     |
| `docker ps -a`                                  | Lista todos los contenedores, activos e inactivos.    |
| `docker rm <contenedor>`                        | Elimina un contenedor específico.                     |
| `docker images`                                 | Lista todas las imágenes locales.                     |
| `docker inspect <objeto>`                        | Muestra detalles de un contenedor o imagen.           |
| `docker system info`                            | Proporciona información general sobre Docker.         |
| `docker system prune`                           | Limpia recursos no utilizados.                        |
| `docker exec -it <contenedor> <cmd>`            | Ejecuta un comando dentro de un contenedor.           |
| `docker save -o archivo.tar <imagen>`            | Guarda una imagen en un archivo tar.                  |
| `docker load -i archivo.tar`                    | Carga una imagen desde un archivo tar.                |
| `docker search <término>`                       | Busca imágenes en Docker Hub.                         |
| **Actualización de Docker Compose**             | Actualiza `docker-compose` a la última versión.        |
| `docker cp <host_path> <container>:<container_path>` | Copia archivos desde el host al contenedor.      |
| `docker cp <container>:<container_path> <host_path>` | Copia archivos desde el contenedor al host.      |

