# Pwncat-cs Cheat Sheet

#### Reverse shell (Linux)
```
pwncat-cs -lp <PORT>
```

#### Conexión a una máquina Windows
```
pwncat-cs -m windows <IP>
```

#### Conexión a un SSH Server
```
pwncat-cs <USER>@<HOST>
```

#### Conexión a un SSH Server a través del archivo de identidad
```
pwncat-cs -i <RSA_FILE> <USER>@<HOST>
```

#### Listar conexiones persistentes
```
pwncat-cs --list
```

#### Conectarse a una conexión persistente
```
pwncat-cs <ID>
```

### Modulos

*Una vez con la conexión de pwncat-cs:*

#### Buscar modulos
```
search <WORD>
```

#### Visualizar modulos
```
info <MODULE_NAME>
```

#### Ejecutar modulos
```
run <MODULE_NAME>
```

#### Ejecutar enumeración de datos
```
run enumerate
```

#### Listar y ejecutar la escalación de privilegios
```
escalate list
escalate run
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)