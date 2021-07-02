# Enum4Linux Cheat Sheet

#### Obtener información del NetBIOS
```
enum4linux -u <User> -p <Password> -n <IP-Address>
```

#### Obtener lista de usuarios
```
enum4linux -u <User> -p <Password> -U <IP-Address>
```

#### Enumerar Sistema Operativo
```
enum4linux -u <User> -p <Password> -o <IP-Address>
```

#### Enumerar Politicas de Password
```
enum4linux -u <User> -p <Password> -P <IP-Address>
```

#### Enumerar Politica de Grupo
```
enum4linux -u <User> -p <Password> -G <IP-Address>
```

#### Enumerar Carpetas Compartidas
```
enum4linux -u <User> -p <Password> -S <IP-Address>
```

#### Obtener información limitada sobre la ejecución de LDAP
```
enum4linux -u <User> -p <Password> -l <IP-Address>
```

#### Enumerar Impresoras compartidas
```
enum4linux -u <User> -p <Password> -i <IP-Address>
```

#### Enumerar todo
```
enum4linux -u <User> -p <Password> -a <IP-Address>
```

#### Adivinar por Fuerza Bruta los nombres de los recursos compartidos
```
enum4linux -s /usr/share/enum4linux/share-list.txt <IP-Address>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)