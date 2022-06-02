# File command Cheat Sheet

#### Determinar el tipo de un archivo
```
file <FILE-NAME>
```

#### Mostrar solamente el tipo de archivo
```
file -b <FILE-NAME>
```

#### Mostrar el tipo de archivo de todos lo archivos dentro de un directorio
```
file *
```

#### Mostrar el tipo de archivo de todos lo archivos dentro de un directorio y que no muestre sangria de separación
```
file -N *
```

#### Mostrar el tipo de archivo de todos lo archivos dentro de un directorio en particular
```
file <DIRECTORY-NAME>/*
```

#### Mostrar el tipo de archivo de los archivos que inicien con un tipo de rango de letras
```
file [a-d]*
```

#### Mostrar el tipo de archivo y separar con un string el nombre del archivo y el tipo
```
file -F " * " <FILE-NAME>
```

#### Mostrar el tipo de MIME de un archivo
```
file -i <FILE-NAME>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)