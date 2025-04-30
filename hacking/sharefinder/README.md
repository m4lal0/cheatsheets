# ShareFinder Cheat Sheet

#### Enumerar recursos compartidos usando un usuario autenticado
```
sharefinder auth --username <DOMAIN>\\<USER> -p <PASSWORD> <IP-TARGET>
```

#### Enumerar recursos compartidos usando un usuario autenticado y mostrar el contenido de cada directorio que se tenga lectura
```
sharefinder auth --username <DOMAIN>\\<USER> -p <PASSWORD> <IP-TARGET> --list
```

#### Enumerar recursos compartidos usando un usuario autenticado y guardar los resultados en un archivo (RAW y XML)
```
sharefinder auth --username <DOMAIN>\\<USER> -p <PASSWORD> <IP-TARGET> -o <OUTPUT>
```

#### Enumerar recursos compartidos usando un usuario autenticado y guardar los resultados en un archivo HTML
```
sharefinder auth --username <DOMAIN>\\<USER> -p <PASSWORD> <IP-TARGET> -o <OUTPUT> --html
```

#### Enumerar recursos compartidos de manera anonima
```
sharefinder anon <IP-TARGET>
```

#### Buscar recursos compartidos en toda la red del dominio usando un usuario autenticado
```
sharefinder hunt --username <DOMAIN>\\<USER> -p <PASSWORD> <IP-TARGET>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)