# GetADUsers Cheat Sheet

#### Listar usuarios de AD
```
impacket-GetADUsers <DOMAIN>/ -dc-ip <IP-TARGET> -debug
```

#### Listar usuarios de AD teniendo una cuenta de un usuario
```
impacket-GetADUsers <DOMAIN>/<USER>:<PASSWORD> -dc-ip <IP-TARGET> -all
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)