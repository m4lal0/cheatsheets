# TestSSL Cheat Sheet

#### Escaneo general de SSL y guardar el resultado en un archivo HTML
```
testssl.sh --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

#### Escaneo general de SSL, leyendo desde un archivo los objetivos y guardar el resultado en un archivo HTML
```
testssl.sh --htmlfile <REPORT.html> -iL <FILE-NAME>
```

#### Escanear la seguridad de las cabeceras HTTP y guardar el resultado en un archivo HTML
```
testssl.sh --headers --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

#### Escanear el SSL con todas las vulnerabilidades y guardar el resultado en un archivo HTML
```
testssl.sh --vulnerable --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)