# ps Cheat Sheet

#### Enumerar todos los procesos del sistema
```
ps -aux
```

#### Enumerar todos los procesos del sistema en formato árbol
```
ps -axjf
```

#### Enumerar los procesos propiedad del ususario m4lal0
```
ps -aum4lal0
```

#### Enumerar los procesos propiedad del ususario actual
```
ps -U $USER
```

#### Enumerar todos los procesos con un formato definido
```
ps -eo pid,user,command
```

#### Enumerar los procesos que ejecuta un conjunto de usuarios
```
ps -f -u username1,username2...usernameN
```

#### Mostrar una lista de procesos con un ID padre en particular (5589)
```
ps -f -ppid 5589
```

#### Mostrar una lista de procesos con un conjunto de ID
```
ps -f -p 25001,4567,789
```

#### Ordene los procesos según el uso de la CPU y la memoria (útil para encontrar pérdidas de memoria).
```
ps -aux --sort pmem
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)