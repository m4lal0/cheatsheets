# SMBclient Cheat Sheet

#### Enumerar lo que comparte un Host
```
smbclient -L //10.130.40.80 -N
```

#### Enumerar lo que comparte un Host en un puerto diferente
```
smbclient -L //10.130.40.80 -N -p <PORT>
```

#### Enumerar lo que comparte un Host usando el Nombre de grupo, usuario vacio y sin password
```
smbclient -L <Group-Name> -I <IP-Address> -N -U ""
```

#### Verificar si es vulnerable a Null Sessions
```
smbclient //10.130.40.80/IPC$ -N
smbclient //10.130.40.80/C$ -N
```

#### Acceder y ver los archivos de una carpeta compartida (llamada WorkSharing)
```
smbclient \\\\10.130.40.80\\WorkSharing -N
```

#### Acceder y ver los archivos de una carpeta compartida (llamada secret) proporcionando un usuario y en un puerto diferente
```
smbclient \\\\10.130.40.80\\WorkSharing -U <USER> -p <PORT>
```

#### Acceder a directorio usando un Hash NTLM
```
smbclient \\\\10.130.40.80\\WorkSharing -U '<USER>' --pw-nt-hash '<NTLM-HASH>'
```

#### Acceder a directorio usando un Hash NTLM
```
smbclient //10.10.129.140/Users -U '<USER>' --password='<NTLM-HASH' --pw-nt-hash
```

### Listar carpetas compartidas colocando un protocolo
```
smbclient -L <IP-ADDRESS> -N --option 'client min protocol = NT1'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)