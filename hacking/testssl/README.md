# TestSSL Cheat Sheet

#### Escaneo general de SSL 
```
testssl.sh <HOST|HOST:PORT|URL|URL:PORT>
```

#### Escaneo general de SSL usando el binario de OpenSSL desde otra dirección
```
testssl.sh --openssl=/usr/bin/openssl <HOST|HOST:PORT|URL|URL:PORT>
```

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
ó
testssl.sh -h -oH <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

#### Escanear el SSL con todas las vulnerabilidades y guardar el resultado en un archivo HTML
```
testssl.sh --vulnerable --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
ó
testssl.sh -U -oH <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

#### Escanear que protocolos y versiones usa el SSL y guardar el resultado en un archivo HTML
```
testssl.sh --protocols --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
ó
testssl.sh -p -oH <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

#### Mostrar información del certificado SSL y guardar el resultado en un archivo HTML
```
testssl.sh --server-defaults --htmlfile <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
ó
testssl.sh -S -oH <REPORT.html> <HOST|HOST:PORT|URL|URL:PORT>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)