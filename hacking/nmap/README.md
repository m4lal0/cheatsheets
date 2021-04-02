# NMAP Cheat Sheet

### Scan types

- `-sA`: Escaneo ACK
- `-sP`: Escaneo con Ping 
- `-sR`: Escaneo RPC
- `-sS`: Escaneo SYN "Half-open"
- `-sT`: Escaneo TCP
- `-sU`: Escaneo UDP
- `-sW`: Escaneo a equipos Windows
- `-sn`: Deshabilitar Escaneo de puertos (ping sweep)
- `-sX`: Escaneo XMAS
- `-sN`: Escaneo NULL de TCP
- `-sF`: Escaneo TCP FIN
- `-sM`: Escaneo TCP Maimon
- `-sl`: Escaneo IDLE/IPID Header
- `-sY`: Escaneo SCTP INIT
- `-sZ`: Escaneo SCTP COOKIE ECHO
- `-PR`: Escaneo ARP ping
- `-PU`: Escaneo UDP ping
- `-PE`: Escaneo ICMP ECHO ping
- `-PE <IP-Range>`: Escaneo ICMP ECHO ping sweep
- `-PP`: Escaneo ICMP timestamp ping
- `-PM`: Escaneo ICMP address mask ping
- `-PS`: Escaneo TCP SYN ping
- `-PA`: Escaneo TCP ACK ping
- `-PO`: Escaneo IP Protocol ping

### Scan options

- `-p<Port-Range>`: Rango de puertos
- `-p-`: Escaneo de todos los puertos
- `-pU:53,U:110,T20-445`: Escaneo mixto TCP y UDP
- `--top-ports <number>`: Escaneo del top de puertos especificados
- `--open`: Escaneo de puertos abiertos
- `-F`: Escaneo rápido (Escanea los 100 puertos más populares)
- `--spoof-mac <MAC>`: Envia tramas ethernet a la dirección MAC especificada
- `-e <interface>`: Define Interfaz
- `--interactive`: Modo interactivo

### Service/Version Detection

- `-sV`: Información de Servicio/Versión

### Input options

- `-iL <filename>`: Escaneo de objetivos desde un archivo
- `-iR <num-hosts>`: Escaneo aleatorio de hosts
- `--execlude <host1[host2]...>`: Excluir escaneo de hosts
- `--execlude <filename>`: Escluir del escaneo desde un archivo con listado de hosts.

### Output options

- `-oN`: Formato estandar NMAP
- `-oX`: Formato XML
- `-oG`: Formato grepeable
- `-oS`: Formato Script Kiddies
- `-oA`: Salida en 3 formatos (Normal, XML y Grepeable)

### OS detection

- `-A`: Detección de SO, version, script de escaneo y traceroute
- `-O`: Detección de SO
- `--osscan-guess`: Detección de OS manera agresivo

### Timing

- `-T0`: Paranoico
- `-T1`: Disimulado
- `-T2`: Cortes
- `-T3`: Normal
- `-T4`: Agresivo
- `-T5`: Rápido e intrusivo
- `--max-rate <number>`: Envia paquetes no más lento que 'cantidad' por segundo
- `--min-rate <number>`: Envia paquetes no más rápido que 'cantidad' por segundo

### Misc

- `-V`: Imprime la version de NMAP
- `-N`: Resolución DNS
- `-R`: Reverse Lookup
- `-n`: No resolución DNS
- `-Pn`: Deshabilitar descubrimiento de host. Solamente escaneo de puertos
- `-6`: Habilitar IPv6
- `--scan-delay <time>ms`: Agrega un retraso entre los paquetes enviados
- `--badsum`: Genera una suma de comprobación no válida para paquetes
- `-h`: Panel de Ayuda

### NSE scripts

- `-sC`: Escanear con scripts NSE por default
- `--script default`: Escanear con scripts NSE por default
- `--script <Script-Name>`: Escanear con un script en particular
- `--script <NSE-Categories>`: Escanear con algunas categorias de NSE
- `--script-args <Script-Name>.<Argument>`: Si algun script requiere algun argumento
- `--script-help <script-name>`: Mostrar la ayuda del script a usar
- `--script-updatedb`: Actualizar la base de datos de scripts

### Firewall/IDS Evasion

- `-f`: Fragmentación de paquetes
- `-g <Port-Number>`: Manipulación del puerto origen
- `--mtu <Number>`: Fragmentación más controlada de paquetes
- `-D`: Escaneo de señuelos
- `RND:<Number>`: Genera direcciones IP aleatorias y no reservadas. 
- `--data <Hexadecimal>`: Para enviar los datos binarios (0's y 1's) como cargas útiles en los paquetes enviados
- `--data-length <Number>`: Agrega datos aleatorios a los paquetes enviados
- `--data-string <String>`: Para enviar una cadena regular como cargas útiles en los paquetes enviados a la máquina de destino
- `--randomize-host`: Para escanear la cantidad de hosts en la red de destino en orden aleatorio
- `--badsum`: Para enviar los paquetes con sumas de comprobación TCP/UPD erróneas o falsas al objetivo previsto para evitar ciertos conjuntos de reglas de firewall

### Script Categories

- `locate .nse | xargs grep "categories" | grep -oP '".*?"' | sort -u` - Listar las categorias de NSE
- `/usr/share/nmap/scripts`: Directorio donde estan almacenados los script en Linux
- *safe*: - No afectará al objetivo
- *intrusive*: - No seguro: es probable que afecte al objetivo
- *vuln*: - Escanear en busca de vulnerabilidades
- *exploit*: - Intento de aprovechar una vulnerabilidad
- *auth*: - Intente omitir la autenticación para los servicios en ejecución (por ejemplo, inicie sesión en un servidor FTP de forma anónima)
- *brute*: - Intento de usar la fuerza bruta de las credenciales para ejecutar servicios
- *discovery*: - Intente consultar los servicios en ejecución para obtener más información sobre la red (por ejemplo, consultar un servidor SNMP).

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)