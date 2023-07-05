# Airolib-ng Cheat Sheet

#### Crear fichero de diccionario a usar
```
airolib-ng <PASSWORD-OUTPUT-NAME> --import passwd <WORDLIST>
```

#### Sincronizar con un archivo que contiene el nombre de la red inalámbrica
```
airolib-ng <PASSWORD-OUTPUT-NAME> --import essid essid.lst
```

#### Comprobar que todo este definido
```
airolib-ng <PASSWORD-OUTPUT-NAME> --stats
```

#### Limpiar archivo
```
airolib-ng <PASSWORD-OUTPUT-NAME> --clean all
```

#### Generar claves precomputadas
```
airolib-ng <PASSWORD-OUTPUT-NAME> --batch
```

#### Usar las claves precomputadas para crackear contraseña
```
aircrack-ng -r <PASSWORD-OUTPUT-NAME> <CAPTURE-NAME>.cap
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)