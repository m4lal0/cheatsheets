# wget Cheat Sheet

#### Descargar un archivo
```
wget <URL-FILE>
```

#### Descargar un archivo y guardarlo con otro nombre
```
wget <URL-FILE> -O <FILE-NAME>
```

#### Descargar especificando un directorio
```
wget -P home/ <URL>
```

#### Descargar de manera recursiva
```
wget -r <URL>
```

#### Descargar de manera recursiva y solamente archivos jpg y png
```
wget -r -A jpg,png <URL>
```

#### Descargar de manera recursiva con excepción de archivos jpg y png
```
wget -r -R jpg,png <URL>
```

#### Descargar todos los archivos PDF de un sitio
```
wget -m -A ".pdf" -nd -e robots-off <URL>
```

#### Descargar el espejo de un sitio
```
wget -m <URL>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)