# Strings Cheat Sheet

#### Extraer las cadenas de texto de un archivo binario
```
strings <File>
```

#### Extraer las cadenas de texto de un archivo binario configuracion la longitud minima
```
strings -n <Length> <File>
```

#### Extraer las cadenas de texto de un archivo binario incluyendo espacios en blanco
```
strings -w <File>
```

#### Extraer las cadenas de texto de varios archivos binarios
```
strings -f /bin/*
```

#### Extraer las cadenas de texto de un archivo binario mostrando el codificado a 16 bits
```
strings -e l /bin/*
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)