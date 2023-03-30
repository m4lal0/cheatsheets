# LookupSID Cheat Sheet

#### Enumerar usuarios locales del dominio con null session
```
impacket-lookupsid <DOMAIN>/anonymous@<IP-TARGET> | cut -d " " -f2
```

#### Enumerar usuarios locales del dominio, teniendo un usuario y contraseña
```
impacket-lookupsid <DOMAIN>/<USER>:"<PASSWORD>"@<IP-TARGET> | cut -d " " -f2
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)