# LDAPHunter Cheat Sheet

#### Obtener toda información de LDAP usando una autenticación de usuario de Dominio
```
python3 ldap_hunter.py -s <IP-TARGET> -d <DOMAIN> -u '<USER>' -P '<PASSWORD>'
```

#### Obtener toda información de LDAP de forma anonima
```
python3 ldap_hunter.py -s <IP-TARGET> -d <DOMAIN> -no-auth
```

#### Obtener toda información de LDAP usando una autenticación de usuario de Dominio y por el puerto 636 que es LDAPS
```
python3 ldap_hunter.py -s <IP-TARGET> -d <DOMAIN> -u '<USER>' -P '<PASSWORD>' --ssl
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)