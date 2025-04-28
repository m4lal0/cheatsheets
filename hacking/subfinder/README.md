# Subfinder Cheat Sheet

#### Enumerar subdominios
```
subfinder -d <Domain> -all
```

#### Enumerar subdominios, mostrando solo los que encuentra y usando una concurrencia de 50
```
subfinder -d <Domain> -silent -t 50
```

#### Enumerar subdominios desde un archivo con una lista de Dominios y guardarlo en un archivo
```
subfinder -dL <File> -o <File>
```

#### Enumerar subdominios desde un archivo con una lista de Dominios y guardarlo en un directorio especifico
```
subfinder -dL <File> -oD <Path/to/file>
```

#### Obtener los resultados en formato JSON y guardar el resultado en un archivo
```
subfinder -d <Domain> -o <File> -oJ -nW
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)