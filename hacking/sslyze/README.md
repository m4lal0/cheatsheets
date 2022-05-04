# SSLyze Cheat Sheet

#### Escaneo de servicios SSL a un sitio Web
```
sslyze -regular <HOST>
```

#### Escaneo de servicios SSL a un sitio Web y guardar los resultados en un archivo JSON
```
sslyze -regular <HOST> --json_out <JSON-FILE.json>
```

#### Escaneo de servicios SSL leyendo un listado de diferentes sitios web con el formato host:port
```
sslyze -regular --targets_in <HOSTS-FILE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)