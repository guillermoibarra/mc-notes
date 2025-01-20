## Introducción a pyenv

En el **Curso de Monte Carlo**, es fundamental gestionar eficazmente las versiones de Python y los entornos virtuales para asegurar un desarrollo coherente y libre de conflictos. Para lograr esto, utilizamos **pyenv**, una herramienta poderosa y flexible que facilita la administración de múltiples versiones de Python y la creación de entornos virtuales aislados. A continuación, exploraremos qué es pyenv, cómo funciona y los beneficios que aporta específicamente a nuestro curso.

### ¿Qué es pyenv?

**pyenv** es una herramienta de gestión de versiones de Python que permite instalar, cambiar y administrar múltiples versiones de Python en un solo sistema de manera sencilla. Con pyenv, puedes alternar entre diferentes versiones de Python para diferentes proyectos, asegurando que cada proyecto utilice la versión adecuada sin interferencias.

### ¿Cómo Funciona pyenv?

pyenv funciona interceptando los comandos relacionados con Python y redirigiéndolos a la versión de Python especificada por el usuario. Se integra con el sistema mediante ajustes en el archivo de configuración del shell (como `.zshrc`), lo que permite cambiar de versión de Python de manera dinámica según el directorio de trabajo o la configuración del proyecto.

#### Componentes Clave de pyenv

- **pyenv**: El núcleo de la herramienta que gestiona las versiones de Python.
- **pyenv-virtualenv**: Un plugin para pyenv que facilita la creación y gestión de entornos virtuales.
- **Shims**: Pequeños scripts que interceptan las llamadas a Python y redirigen a la versión correcta.

### Beneficios de Usar pyenv en Este Curso

Integrar pyenv en nuestro flujo de trabajo del Curso de Monte Carlo ofrece múltiples ventajas que mejorarán tu experiencia de desarrollo:

1. **Gestión Sencilla de Múltiples Versiones de Python**
   
   pyenv permite instalar y utilizar múltiples versiones de Python en el mismo sistema sin conflictos. Esto es especialmente útil cuando trabajamos con diferentes proyectos que requieren versiones específicas de Python.

2. **Entornos Virtuales Aislados**
   
   Con pyenv-virtualenv, puedes crear entornos virtuales aislados para cada proyecto, asegurando que las dependencias y paquetes instalados no afecten a otros proyectos. Esto promueve las mejores prácticas de desarrollo y evita problemas de compatibilidad.

3. **Flexibilidad y Control**
   
   Puedes cambiar fácilmente la versión de Python a nivel global, por directorio o por proyecto, proporcionando un control granular sobre tu entorno de desarrollo.

4. **Facilidad de Instalación y Uso**
   
   pyenv simplifica la instalación de nuevas versiones de Python y la creación de entornos virtuales con comandos sencillos, eliminando la necesidad de configuraciones manuales complejas.

5. **Compatibilidad con Docker**
   
   Aunque utilizamos Docker para encapsular nuestros entornos, pyenv es igualmente útil para gestionar entornos de desarrollo locales, facilitando el desarrollo y las pruebas fuera de los contenedores Docker.

6. **Mejora de la Productividad**
   
   Al automatizar la gestión de versiones y entornos, pyenv te permite enfocarte más en el desarrollo y menos en la configuración del entorno, aumentando tu eficiencia y productividad.

## Cheatsheet de Comandos de pyenv

### Comandos Generales

| Comando                               | Descripción                                              |
|---------------------------------------|----------------------------------------------------------|
| `pyenv install <versión>`             | Instala una versión específica de Python.                |
| `pyenv uninstall <versión>`           | Desinstala una versión específica de Python.             |
| `pyenv versions`                      | Lista todas las versiones de Python instaladas.          |
| `pyenv global <versión>`               | Establece la versión global de Python.                   |
| `pyenv local <versión>`                | Establece la versión de Python para el directorio actual.|
| `pyenv shell <versión>`                | Establece la versión de Python para la sesión actual.    |
| `pyenv rehash`                        | Recalcula los shims de pyenv (usualmente automático).    |
| `pyenv which <comando>`                | Muestra la ruta del ejecutable para un comando dado.     |

### Comandos de Entornos Virtuales (pyenv-virtualenv)

| Comando                                     | Descripción                                             |
|---------------------------------------------|---------------------------------------------------------|
| `pyenv virtualenv <versión> <nombre_env>`    | Crea un entorno virtual con la versión especificada.    |
| `pyenv virtualenv-delete <nombre_env>`       | Elimina un entorno virtual específico.                  |
| `pyenv activate <nombre_env>`                | Activa el entorno virtual especificado.                 |
| `pyenv deactivate`                           | Desactiva el entorno virtual activo.                    |
| `pyenv virtualenvs`                          | Lista todos los entornos virtuales creados.             |

### Comandos de Navegación y Gestión

| Comando                                         | Descripción                                             |
|-------------------------------------------------|---------------------------------------------------------|
| `pyenv version`                                 | Muestra la versión actual de Python utilizada.          |
| `pyenv version-name`                            | Muestra solo el nombre de la versión actual.            |
| `pyenv global`                                  | Muestra la versión global de Python establecida.        |
| `pyenv local`                                   | Muestra la versión de Python establecida localmente.    |
| `pyenv shell`                                   | Muestra la versión de Python establecida para la sesión.|

### Comandos Avanzados

| Comando                                         | Descripción                                             |
|-------------------------------------------------|---------------------------------------------------------|
| `pyenv update`                                  | Actualiza pyenv a la última versión disponible.         |
| `pyenv doctor`                                  | Ejecuta un script para verificar la instalación de pyenv.|
| `pyenv exec <comando>`                          | Ejecuta un comando usando la versión de Python seleccionada.|

### Ejemplos Prácticos

| Ejemplo de Comando                                  | Descripción                                             |
|-----------------------------------------------------|---------------------------------------------------------|
| `pyenv install 3.8.10`                               | Instala Python versión 3.8.10.                           |
| `pyenv global 3.8.10`                                | Establece Python 3.8.10 como la versión global.          |
| `pyenv virtualenv 3.8.10 montecarlo-env`             | Crea un entorno virtual llamado `montecarlo-env` con Python 3.8.10. |
| `pyenv activate montecarlo-env`                      | Activa el entorno virtual `montecarlo-env`.             |
| `pyenv deactivate`                                   | Desactiva el entorno virtual activo.                    |
| `pyenv uninstall 3.8.10`                             | Desinstala Python versión 3.8.10.                        |
| `pyenv virtualenv-delete montecarlo-env`             | Elimina el entorno virtual `montecarlo-env`.            |

