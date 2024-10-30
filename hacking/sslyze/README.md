# SSLyze Cheat Sheet

#### Escaneo de servicios SSL a un sitio Web
```
sslyze -regular <HOST>
```

#### Escaneo de servicios SSL a un sitio Web y guardar los resultados en un archivo JSON
```
sslyze -regular <HOST> --json_out <JSON-FILE>.json
```

#### Escaneo de servicios SSL leyendo un listado de diferentes sitios web con el formato host:port
```
sslyze -regular --targets_in <HOSTS-FILE>
```

### Escaneo diferentes versiones de TLS/SSL, openSSL, vulnerabilidades e información del certificado
```
sslyze --sslv2 --sslv3 --tlsv1 --tlsv1_1 --tlsv1_2 --tlsv1_3 --certinfo --reneg --compression --heartbleed --openssl_ccs --fallback --robot <HOST> --json_out <JSON-FILE>.json
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)