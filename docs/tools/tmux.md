## Introducción a tmux

Para mejorar tu productividad y gestionar múltiples tareas de manera eficiente en el terminal, **tmux** (Terminal Multiplexer) es una herramienta esencial. En esta sección, aprenderás qué es tmux, cómo funciona, sus conceptos clave como sesiones, ventanas y paneles (panes), y un cheatsheet de comandos básicos para comenzar a utilizarlo eficazmente. Además, se incluye una configuración personalizada donde la tecla líder está definida como **Ctrl + Space**.

### ¿Qué es tmux?

**tmux** es un multiplexor de terminal que te permite crear y gestionar múltiples sesiones de terminal dentro de una sola ventana de terminal. Con tmux, puedes dividir tu terminal en múltiples paneles, cada uno ejecutando diferentes procesos o tareas, y mantener estas sesiones activas incluso si cierras la ventana del terminal o te desconectas del sistema.

#### Ventajas de Usar tmux

- **Multiplexación de Terminales**: Ejecuta múltiples sesiones de terminal en una sola ventana.
- **Persistencia de Sesiones**: Mantén tus sesiones activas incluso después de cerrar el terminal.
- **Organización Eficiente**: Divide tu terminal en paneles y ventanas para una mejor gestión de tareas.
- **Personalización**: Configura tmux según tus preferencias para optimizar tu flujo de trabajo.

## Resumen de Comandos Clave

### Comandos Generales

| Comando                                | Descripción                                         |
|----------------------------------------|-----------------------------------------------------|
| `tmux new -s <nombre_sesion>`          | Crea una nueva sesión con el nombre especificado.   |
| `tmux ls`                              | Lista todas las sesiones activas.                   |
| `tmux attach -t <nombre_sesion>`       | Adjunta a una sesión existente.                     |
| `tmux detach`                          | Separa la sesión actual sin cerrarla.               |
| `tmux kill-session -t <nombre_sesion>` | Elimina una sesión específica.                      |

### Atajos de Teclado

> **Nota**: Todos los atajos comienzan con la tecla líder **Ctrl + Space**.

| Atajo                                 | Acción                                                      |
|---------------------------------------|-------------------------------------------------------------|
| `Ctrl + Space, c`                     | Crea una nueva ventana.                                     |
| `Ctrl + Space, n`                     | Navega a la siguiente ventana.                              |
| `Ctrl + Space, p`                     | Navega a la ventana anterior.                               |
| `Ctrl + Space, <número>`              | Selecciona la ventana por su número.                        |
| `Ctrl + Space, %`                     | Divide la ventana actual horizontalmente en dos paneles.    |
| `Ctrl + Space, "`                     | Divide la ventana actual verticalmente en dos paneles.      |
| `Ctrl + Space, Flecha (← ↑ → ↓)`      | Navega entre paneles en la dirección de la flecha.          |
| `Ctrl + Space, x`                     | Cierra el panel actual.                                     |
| `Ctrl + Space, d`                     | Separa la sesión actual (detach).                           |
| `Ctrl + Space, ?`                     | Muestra una lista de todos los atajos de teclado disponibles. |

### Gestión de Ventanas y Paneles

| Comando                                | Descripción                                         |
|----------------------------------------|-----------------------------------------------------|
| `Ctrl + Space, c`                      | Crea una nueva ventana.                             |
| `Ctrl + Space, n`                      | Navega a la siguiente ventana.                      |
| `Ctrl + Space, p`                      | Navega a la ventana anterior.                       |
| `Ctrl + Space, <número>`                | Selecciona la ventana por su número.                |
| `Ctrl + Space, %`                      | Divide la ventana actual horizontalmente.           |
| `Ctrl + Space, "`                      | Divide la ventana actual verticalmente.             |
| `Ctrl + Space, Flecha (← ↑ → ↓)`       | Cambia el enfoque al panel en la dirección de la flecha. |
| `Ctrl + Space, o`                      | Alterna entre los paneles dentro de una ventana.     |
| `Ctrl + Space, x`                      | Cierra el panel actual.                             |

### Comandos de Navegación

| Comando                                | Descripción                                         |
|----------------------------------------|-----------------------------------------------------|
| `Ctrl + Space, h`                      | Selecciona el panel a la izquierda.                 |
| `Ctrl + Space, j`                      | Selecciona el panel inferior.                       |
| `Ctrl + Space, k`                      | Selecciona el panel superior.                       |
| `Ctrl + Space, l`                      | Selecciona el panel a la derecha.                   |

### Otros Comandos Útiles

| Comando                                | Descripción                                         |
|----------------------------------------|-----------------------------------------------------|
| `Ctrl + Space, d`                      | Separa la sesión actual (detach).                   |
| `Ctrl + Space, ?`                      | Muestra ayuda y lista de atajos disponibles.        |
| `Ctrl + Space, t`                      | Muestra la hora en la barra de estado de tmux.      |
| `Ctrl + Space, s`                      | Lista todas las sesiones activas.                   |

