# SMBServer Cheat Sheet

#### Lanzar un SMB Server con nombre Kali y que comparta el directorio actual con usuario y password para accesar
```
smbserver.py -username <Username> -password <Password> -smb2support Kali ${pwd}
```

#### Crear un SMB Server en el directorio actual sin credenciales de acceso
```
smbserver.py smbFolder $(pwd) -smb2support
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)