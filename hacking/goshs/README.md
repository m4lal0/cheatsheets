# goshs Cheat Sheet

#### Levantar un webserver en el directorio de trabajo actual
```
goshs
```

#### Levantar un webserver en el directorio de trabajo actual usando un puerto en especifico
```
goshs -p <PORT>
```

#### Levantar un webserver en un directorio de trabajo dado y usando un puerto en especifico
```
goshs -p <PORT> -d <DIRECTORY-PATH>
```

#### Levantar un webserver en solo modo lectura (no permite cargar archivos)
```
goshs -ro
```

#### Levantar un webserver que solo permita cargar archivos y no permite descargar nada
```
goshs -uo
```

#### Levantar un webserver usando una autenticación basica HTTP
```
goshs -b <USER:PASSWORD>
```

#### Levantar un webserver con soporte de WEBDAV en el directorio de trabajo actual
```
goshs -w
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)