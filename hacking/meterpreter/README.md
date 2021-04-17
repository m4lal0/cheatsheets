# Meterpreter Cheat Sheet

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`sysinfo`**      | Mostrar información del sistema       |
| **`ps`**      | Lista y muestra procesos en ejecución       |
| **`upload`**      | Cargar un archivo       |
| **`download`**      | Descargar un archivo       |
| **`pwd`**      | Mostrar directorio de trabajo (remoto)       |
| **`lpwd`**      | Mostrar directorio de trabajo (local)       |
| **`cd`**      | Cambiar directorio (remoto)       |
| **`lcd`**      | Cambiar directorio (local)       |
| **`cat`**      | Mostrar contenido del archivo       |
| **`mkdir`**      | Crear un directorio       |
| **`rmdir`**      | Eliminar un directorio       |
| **`bglist`**      | Mostrar scripts en ejecución en segundo plano       |
| **`bgrun`**      | Hacer que un script se ejecute en segundo plano       |
| **`bgkill`**      | Terminar un proceso en segundo plano       |
| **`background`**      | Mover sesión activa al segundo plano       |
| **`edit`**      | Editar un archivo en el editor vi       |
| **`del`**      | Eliminar un archivo       |
| **`idletime`**      | Mostrar el tiempo de inactividad del usuario       |
| **`screenshot`**      | Tomar una captura de pantalla       |
| **`clearev`**      | Borrar los registros del sistema       |
| **`?`**      | Comando disponibles       |
| **`exit` / `quit`**      | Salir de la sesión de Meterpreter       |
| **`shutdown` / `reboot`**      | Reiniciar el sistema       |
| **`use`**      | Carga de extensión       |
| **`load <ModuleName>`**      | Carga un módulo de meterpreter especial para ataques avanzados        |
| **`load -l`**      | Visualizar módulos que podemos cargar y usar        |
| **`search -f <FileName.Extension>`**      | Busca un archivo en la máquina destino       |
| **`channel`**      | Mostrar canales activos       |

### Comando Administrador de contraseña

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`hashdump`**      | Muestra los hashes del sistema       |

### Comandos de Red

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`ipconfig`**      | Mostrar la configuración de la interfaz de red       |
| **`portfwd`**      | Reenviar paquetes       |
| **`route`**      | Ver/Editar tabla de enrutamiento de red       |

### Comandos de Interfaz/Salida

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`enumdesktops`**      | Mostrar todos los escritorios disponibles       |
| **`getdesktop`**      | Mostrar escritorio actual       |
| **`keyscan_start`**      | Iniciar keylogger en la máquina destino       |
| **`keyscan_stop`**      | Detener keylogger en la máquina destino       |
| **`set_desktop`**      | Configurar escritorio       |
| **`keyscan_dump`**      | Volcado de contenido del keylogger       |

### Comandos de Manejo de procesos

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`getpid`**      | Mostrar la ID del proceso       |
| **`getuid`**      | Mostrar la ID de usuario       |
| **`ps`**      | Mostrar procesos en ejecución       |
| **`kill <PID>`**      | Detener y finalizar un proceso en ejecución       |
| **`getprivs`**      | Muestra múltiples privilegios como sea posible       |
| **`reg`**      | Acceder al registro de la máquina destino       |
| **`shell`**      | Acceder al shell de la máquina destino       |
| **`execute`**      | Ejecuta un comando en el destino       |
| **`migrate <PID>`**      | Moverse a un ID de proceso de destino dado       |

### Comandos de Escalada de privilegios

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`use priv`**      | Carga el script       |
| **`getsystem`**      | Eleva tus privilegios       |
| **`getprivs`**      | Eleva tus privilegios       |

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)