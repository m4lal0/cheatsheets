# LookupSID Cheat Sheet

#### Enumerar usuarios locales del dominio con null session
```
impacket-lookupsid anonymous@<DOMAIN> -no-pass | grep SidTypeUser | cut -d' ' -f2 | cut -d'\' -f2 | tr '[:upper:]' '[:lower:]'
```

#### Enumerar usuarios locales del dominio, teniendo un usuario y contraseña
```
impacket-lookupsid <DOMAIN>/<USER>:"<PASSWORD>"@<IP-TARGET> | cut -d " " -f2
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)