# NMAP Cheat Sheet

### Scan types

- `-sA`: Escaneo ACK
- `-sP`: Escaneo con Ping 
- `-sR`: Escaneo RPC
- `-sS`: Escaneo SYN
- `-sT`: Escaneo TCP
- `-sU`: Escaneo UDP
- `-sW`: Escaneo a equipos Windows
- `-sX`: Escaneo XMAS
- `-sn`: Deshabilitar Escaneo de puertos
- `-sN`: Escaneo NULL

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
- `-f`: Fragmentación
- `-N`: Resolución DNS
- `-R`: Reverse Lookup
- `-n`: No resolución DNS
- `-Pn`: Deshabilitar descubrimiento de host. Solamente escaneo de puertos.
- `-6`: Habilitar IPv6
- `-h`: Panel de Ayuda

### NSE scripts

- `-sC`: Escanear con scripts NSE por default
- `--script default`: Escanear con scripts NSE por default
- `--script <NameScript>`: Escanear con un script en particular
- `--script-updatedb`: Actualizar la base de datos de scripts

### Script Categories

- `locate .nse | xargs grep "categories" | grep -oP '".*?"' | sort -u`

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)