# hauditor Cheat Sheet

#### Analizar cabeceras HTTP de seguridad de un sitio web
```
hauditor -t <DOMAIN>
```

#### Analizar cabeceras HTTP de seguridad de varios sitios web a traves de un archivo
```
hauditor -f <FILE>
```

#### Analizar cabeceras HTTP de seguridad de un sitio web y pasar la petición en un proxy
```
hauditor -t <DOMAIN> -p 127.0.0.1:8080
```

#### Analizar cabeceras HTTP de seguridad de un sitio web y especificando alguna cookie
```
hauditor -t <DOMAIN> -c <COOKIE>
```

#### Analizar cabeceras HTTP de seguridad de un sitio web y especificar alguna cabecera
```
hauditor -t <DOMAIN> -r <HEADERS>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)