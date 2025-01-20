# Fundamentos del Terminal Linux con zsh y Starship

En esta sección, aprenderás los fundamentos del uso del terminal en Linux, enfocándonos en **zsh** (Z Shell) y **Starship**, un prompt moderno y altamente configurable. Comprenderás cómo funcionan estas herramientas, cómo se configuran mediante el archivo `.zshrc`, y cómo pueden mejorar tu flujo de trabajo en el entorno Docker configurado para el Curso de Monte Carlo.

## Introducción al Terminal Linux

### ¿Qué es el Terminal?

El **Terminal** es una interfaz de línea de comandos que permite a los usuarios interactuar con el sistema operativo mediante comandos de texto. A diferencia de las interfaces gráficas de usuario (GUI), el terminal ofrece un control más directo y eficiente sobre el sistema.

### Ventajas de Usar el Terminal

- **Eficiencia y Velocidad**: Ejecuta tareas rápidamente sin necesidad de navegar por menús gráficos.
- **Automatización de Tareas**: Crea scripts para automatizar procesos repetitivos.
- **Acceso a Funcionalidades Avanzadas**: Realiza operaciones que no siempre están disponibles en las GUI.

---

## Introducción a zsh

### ¿Qué es zsh?

**zsh** (Z Shell) es un potente intérprete de comandos para sistemas Unix/Linux. Combina las características de otros shells como `bash`, `ksh`, y `tcsh`, ofreciendo mejoras significativas en términos de personalización y funcionalidad.

### Ventajas de Usar zsh

- **Autocompletado Avanzado**: Ofrece sugerencias inteligentes y completado de comandos más robusto.
- **Mejoras en la Personalización**: Permite una configuración altamente personalizada del entorno de trabajo.
- **Integración con Plugins y Temas**: Compatible con frameworks como Oh My Zsh y herramientas como Starship para mejorar la experiencia del usuario.

---

## Configuración de zsh con `.zshrc`

### ¿Qué es el Archivo `.zshrc`?

El archivo `.zshrc` es un script de configuración que se ejecuta cada vez que se inicia una nueva sesión de zsh. Aquí es donde defines variables de entorno, alias, funciones personalizadas, y configuras el prompt, entre otros ajustes.

### Personalización Básica

#### Cambiar el Prompt

El prompt es la línea que ves en el terminal que indica que puedes ingresar un comando. Con zsh y Starship, puedes personalizar este prompt para mostrar información útil como el directorio actual, el estado de Git, etc.

#### Alias

Los alias son atajos para comandos largos o complejos. Por ejemplo:

```zsh
alias ll='ls -la'
alias gs='git status'
alias docker-start='docker-compose up -d
```

## Integración con Starship

Starship es un prompt rápido y personalizable para cualquier shell, incluyendo zsh. Se configura principalmente a través de un archivo de configuración separado (`starship.toml`), pero puede interactuar con `.zshrc` para una integración fluida.

## Navegación Básica en el Terminal

Comandos de Navegación de Directorios:

- `cd <directorio>`: Cambia al directorio especificado.
- `ls`: Lista los archivos y carpetas en el directorio actual.
- `pwd`: Muestra la ruta completa del directorio actual.

Gestión de Archivos y Directorios:

- `cp <origen> <destino>`: Copia archivos o directorios.
- `mv <origen> <destino>`: Mueve o renombra archivos o directorios.
- `rm <archivo>`: Elimina un archivo.
- `mkdir <nombre>`: Crea un nuevo directorio.
- `rmdir <nombre>`: Elimina un directorio vacío.

Visualización y Edición de Archivos:

- `cat <archivo>`: Muestra el contenido de un archivo.
- `less <archivo>`: Permite una visualización paginada de un archivo.
- `nano <archivo>`: Edita un archivo usando el editor Nano.
- `vim <archivo>`: Edita un archivo usando el editor Vim.

## Gestión de Procesos

Listar Procesos:

- `ps`: Muestra los procesos en ejecución.
- `top`: Muestra una lista dinámica de los procesos en ejecución.
- `htop`: Una versión mejorada y más interactiva de top (puede requerir instalación).

Controlar Procesos:
- `kill <PID>`: Termina el proceso con el ID especificado.
- `pkill <nombre>`: Termina procesos por nombre.
- `bg`: Envía un proceso detenido al fondo.
- `fg`: Trae un proceso del fondo al frente.
- `jobs`: Lista los trabajos en segundo plano y detenidos.

## Redirección y Pipes

Redirección de Entrada y Salida:

`>`: Redirige la salida de un comando a un archivo, sobrescribiéndolo.
```bash
echo "Hola Mundo" > hola.txt
```

`>>`: Redirige la salida de un comando a un archivo, agregando al final.
```bash
echo "Otra línea" >> hola.txt
```

`<`: Redirige la entrada de un archivo a un comando.
```bash
wc -l < hola.txt
```

Uso de Pipes para Encadenar Comandos:

`|`: Toma la salida de un comando y la usa como entrada para otro.
```bash
ls -la | grep "Proyecto"
```
