# Webanalyze Cheat Sheet

#### Descargar el archivo de tecnologias de Wappalyzer para que funcione la herramienta
```
webanalyze -update
```

#### Identificar técnologias de un sitio web
```
webanalyze -host <URL>
```

#### Identificar técnologias de un sitio web y no mostrar la cabecera de la aplicación
```
webanalyze -host <URL> -silent
```

#### Identificar técnologias de varios sitios web desde un archivo
```
webanalyze -hosts <URL-FILENAME> -silent
```

#### Identificar técnologias de un sitio web, aplicando redirect
```
webanalyze -host <URL> -redirect -silent
```

#### Identificar técnologias de un sitio web y mostrar el resultado en JSON
```
webanalyze -host <URL> -silent -output json
```

#### Identificar técnologias de un sitio web y mostrar el resultado en CSV
```
webanalyze -host <URL> -silent -output csv
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)