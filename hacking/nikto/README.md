# Nikto Cheat Sheet

### Escanear un host
*Realiza escaneo de un host por medio de su IP o nombre al puerto 80.*
```
nikto -host [IP-ADDRESS/WEBSITE]
```

### Escanear un host si tiene SSL
```
nikto -host [IP-ADDRESS/WEBSITE] -ssl
```

### Escanear un host en multiples puertos
*Escanear un host en diferentes puertos (el puerto por default es el 80).*
```
nikto -host [IP-ADDRESS/WEBSITE] -port [Port1], [Port2], [Port3]
```

### Escaneo con Tuning
```
nikto -host [IP-ADDRESS/WEBSITE] -Tuning 1234bde
```

### Buscar directorios CGI
*Podemos usar filtros como "none" o "all" para escanear todos los directorios CGI o ninguno.*
```
nikto -host [IP-ADDRESS/WEBSITE] -Cgidirs all
```

### Escanear un host y el resultado guardarlo en un formato HTML
*Los distintos tipos de formatos son: csv, json, html, nbe, sql, txt y xml.*
```
nikto -host [IP-ADDRESS/WEBSITE] -Fortmat html -output [FileName]
```

### Escanear un host y mostrar resultados segun las opciones seleccionadas
*Se puede ver en la opción de ayuda los parámetros de Display*
```
nikto -host [IP-ADDRESS/WEBSITE] -Display 1234EP
``` 

### Display Options

- `1` : Show redirects
- `2` : Show cookies received
- `3` : Show all 200/OK responses
- `4` : Show URLs which require authentication
- `D` : Debug output
- `E` : Display all HTTP errors
- `P` : Print progress to STDOUT
- `S` : Scrub output of IPs and hostnames
- `V` : Verbose output

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)