# ad-ldap-enum Cheat Sheet

#### Obtener toda información de LDAP usando una autenticación de usuario de Dominio.
```
python3 ad-ldap-enum.py -d <DOMAIN> -l <IP-TARGET> -u '<USER>' -p '<PASSWORD>'
```

#### Obtener toda información de LDAP usando una autenticación de usuario hash NTLM (Pass-The-Hash).
```
python3 ad-ldap-enum.py -d <DOMAIN> -l <IP-TARGET> -u '<USER>' -p '<LM:NTLM>'
```

#### Obtener toda información de LDAP usando una autenticación de usuario de Dominio y añade una cadena a todos los nombres de archivos de salida.
```
python3 ad-ldap-enum.py -d <DOMAIN> -l <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -o '<TEXT>'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)