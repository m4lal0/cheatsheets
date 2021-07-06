# SMBclient Cheat Sheet

#### Enumerar lo que comparte un Host
```
smbclient -L //10.130.40.80 -N
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

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)