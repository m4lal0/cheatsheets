# Metasploit Cheat Sheet

### Inicializar
| Comando| Uso                    |
| ------------- | ------------------------------ |
| `msfdb init` ó `msfdb run`      | Iniciar Metasploit       |
| `msfconsole`      | Entrar a Metasploit       |

### Usando la BD
| Comando| Uso                    |
| ------------- | ------------------------------ |
| `db_driver`      | Muestra las BD disponibles y la que estamos usando por defecto       |
| `db_status`      | Muestra la conexión a la BD       |
| `db_import`      | Importar los resultados de un escaneo como un archivo XML de Nmap       |
| `db_nmap`      | Realiza un escaneo de puertos de un hosts y los que encuentra abiertos los almacena en la BD       |
| `db_destroy`      | Elimina la BD       |
| `hosts`      | Muestra los hosts guardados en la BD       |
| `services`      | Muestra los servicios y puertos que estan guardados en la BD       |
| `services -p <port-number>`      | Mostrar los hosts que tienen un puerto abierto en especifico       |
| `vulns`      | Muestra todas las vulnerabilidades encontradas       |
| `creds`      | Muestra todas las credenciales encontradas       |

### Comandos generales
| Comando| Uso                    |
| ------------- | ------------------------------ |
| `help`      | Panel de ayuda       |
| `banner`      | Cambia el banner de inicio       |
| `version`      | Muestra la versión de Metasploit       |
| `msfupdate`      | Obtener la actualización semanal       |
| `search <keyword>`      | Busca los exploits con la palabra clave dada       |
| `back`      | Salir del contexto actual en ejecución (exploit o module)       |

### Configuración de Modulos (Exploits/Audiliary/Payloads)
| Comando| Uso                    |
| ------------- | ------------------------------ |
| `use <module>`      | Usar y configurar un exploit       |
| `edit`      | Modificar el codigo del exploit       |
| `show info`      | Muestra la información acerca del exploit       |
| `show options`      | Muestra las opciones generales del exploit seleccionado       |
| `show advanced`      | Muestra las opciones avanzadas del exploit seleccionado       |
| `set <option> <settings>`      | Establecer la configuración deseada       |
| `unset <option> <settings>`      | Elimina el valor actual de una variable del exploit o módulo en uso       |
| `set payload <payload>`      | Configurar el payload a usar       |
| `setg <option> <settings>`      | Define variables globales que serán empleadas por todos los modulos o exploits cargados       |
| `unsetg <option> <settings>`      | Elimina la variable global       |
| `check`      | Comprueba si el objetivo es vulnerable al exploit seleccionado o no       |
| `exploit`      | Ejecutar el exploit cargado       |
| `exploit -j`      | Ejecutar el exploit en segundo plano       |
| `exploit -z`      | Ejecutar el exploit y tras una explotación exitosa no se interactúe con la sesión       |
| `run`      | Ejecutar el módulo/auxiliary cargado       |

### Manejo de sesiones
| Comando| Uso                    |
| ------------- | ------------------------------ |
| `sessions -l`      | Listar todas las sesiones activas       |
| `sessions -i <session-id>`      | Interactuar con una sesión en particular       |
| `sessions -k`      | Finaliza todas las sesiones       |
| `sessions -u <session-id>`      | Actualiza las sesiones a una sesión de meterpreter       |
| `background` ó <kbd>ctrl</kbd> + <kbd>z</kbd>      | Enviar la sesión acutal a background       |
| `jobs`      | Módulos que se encuentran en ejecución en "background", permite listar y terminar comandos existentes       |
| `jobs -k <job-id>`      | Eliminar un job       |


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)