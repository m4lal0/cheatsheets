# Nikto Cheat Sheet

### Escanear un host

- `nikto -host [IPAddress/Name]`: Realiza escaneo de un host por medio de su IP o nombre al puerto 80.

### Escanear un host en multiples puertos

- `nikto -host [IPAddress/Name] -port [Port1], [Port2], [Port3]`: Escanear un host en diferentes puertos (el puerto por default es el 80).

### Escanear un host y el resultado guardarlo en un archivo

- `nikto -host [IPAddress/Name] -output [FileName]`: Guardar el resultado del escaneo en un archivo.

### Escanear un host y el resultado guardarlo en un formato HTML

- `nikto -host [IPAddress/Name] -Fortmat html -output [FileName]`: Los distintos tipos de formatos son: csv, json, html, nbe, sql, txt y xml.

### -Display Options

- `1` : Show redirects
- `2` : Show cookies received
- `3` : Show all 200/OK responses
- `4` : Show URLs which require authentication
- `D` : Debug output
- `E` : Display all HTTP errors