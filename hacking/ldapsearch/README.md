# LDAPSearch Cheat Sheet

#### Enumerar - namingcontext
```
ldapsearch -x -H ldap://<IP-TARGET> -s base namingcontexts
```

#### Enumerar con autenticación - namingcontext
```
ldapsearch -x -H ldap://<IP-TARGET>  -D '<USER>@<DOMAIN>' -w '<PASSWORD>' -s base namingcontexts
```

#### Enumerar - Base de consulta
```
ldapsearch -x -H ldap://<IP-TARGET> -b 'DC=EGOTISTICAL-BANK,DC=LOCAL'
```

#### Enumerar con autenticación - Base de consulta
```
ldapsearch -x -H ldap://<IP-TARGT> -D '<USER>@<DOMAIN>' -w '<PASSWORD>' -b "DC=support,DC=htb"
```

#### Obtener contraseña Administrador - LAPS
```
ldapsearch -x -H ldap://<IP-TARGET> -D '<USER>@<DOMAIN>' -w '<PASSWORD>' -b "dc=streamio,dc=htb" "(ms-MCS-AdmPwd=*)" ms-MCS-AdmPwd
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)