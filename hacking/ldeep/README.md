# ldeep Cheat Sheet

#### Obtener los usuarios del dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' users
```

#### Obtener los usuarios del dominio y guardarlo en un archivo
```
ldeep -o <OUTPUT> ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' users
```

#### Obtener los GPO del dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' gpo
```

#### Obtener las computadoras del dominio y guardarlo en un archivo
```
ldeep -o <OUTPUT> ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' computers
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)