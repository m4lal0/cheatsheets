# Grep Cheat Sheet

#### Busqueda basica de una palabra en un archivo
```
grep 'alias' <FILE_NAME>
```

#### Contar el número de coincidencias
```
grep -c 'error' /var/log/syslog
```

#### Imprimir el número de lineas de coincidencias
```
grep -n 'error' /var/log/syslog
```

#### Buscar archivos que terminan con 'linux'
```
grep -e 'linux$' <FILE_NAME>
```

#### Buscar archivos ignorando mayusculas y minusculas
```
grep -i 'Alias' <FILE_NAME>
```

#### Devuelve los archivos con coincidencias
```
grep -l 'Alias' <PATH_NAME>
```

#### Devuelve los archivos sin coincidencias
```
grep -L 'Alias' <PATH_NAME>
```

#### Busquedas recursivas (subdirectorios)
```
grep -r 'error' <PATH_NAME>
```

#### Seleccionar lineas no coincidentes
```
grep -v 'warning' <FILE_NAME>
```

#### Sólo mostrar la parte de la cadena que coincide
```
grep -o 'warning' <FILE_NAME>
```

#### Imprimir las 6 lineas después del match
```
grep -A 6 'error' <FILE_NAME>
```

#### Imprimir las 2 lineas antes del match
```
grep -B 2 'error' <FILE_NAME>
```

#### Imprimir las 7 lineas antes y después del match
```
grep -C 7 'error' <FILE_NAME>
```

#### Mostrar lineas que contienen bag o beg
```
grep -E 'b(a|e)g' <FILE_NAME>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)