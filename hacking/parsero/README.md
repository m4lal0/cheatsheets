# Parsero Cheat Sheet

#### Leer el archivo robots.txt de un servidor web
```
parsero -u <URL>
```

#### Leer el archivo robots.txt de un servidor web y mostrar solo los que tienen estatus "HTTP 200"
```
parsero -u <URL> -o
```

#### Leer el archivo robots.txt de una lista de servidores web que estan en un archivo
```
parsero -f <FILE>
```

#### Leer el archivo robots.txt de un servidor web y realizar la busqueda en el buscador Bing de lo encontrado
```
parsero -u <URL> -sb
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)