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
ldapsearch -x -H ldap://<IP-TARGT> -D '<USER>@<DOMAIN>' -w '<PASSWORD>' -b "DC=dcname,DC=local"
```

#### Obtener contraseña Administrador - LAPS
```
ldapsearch -x -H ldap://<IP-TARGET> -D '<USER>@<DOMAIN>' -w '<PASSWORD>' -b "dc=streamio,dc=htb" "(ms-MCS-AdmPwd=*)" ms-MCS-AdmPwd
```

#### Mostrar la politica de contraseñas
```
ldapsearch -h <IP-TARGET> -x -b "DC=INLANEFREIGHT,DC=LOCAL" -s sub "*" | grep -m 1 -B 10 pwdHistoryLength
```

#### Listar los usuarios del Directorio Activo
```
ldapsearch -h <IP-TARGET> -x -b "DC=INLANEFREIGHT,DC=LOCAL" -s sub "(&(objectclass=user))"  | grep sAMAccountName: | cut -f2 -d" "
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)