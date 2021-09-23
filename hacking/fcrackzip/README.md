# FcrackZIP Cheat Sheet

#### Fuerza bruta con diccionario y descomprimir el archivo
```
fcrackzip -b -D -p <Wordlist> -u <FileZip>
```

#### Fuerza bruta, con longitud de 3 caracteres, que solo contenga caracteres en minúsculas, $ y %
```
fcrackzip -v -b -l 3 -c 'a:$%' <FileZip>
```

#### Romper contraseñas númericas con una longitud especifica
```
fcrackzip -b -c '1' -l 1-3 -u <FileZip>
```

#### Romper contraseña que sólo contenga dígitos, a partir de la contraseña '12345'
```
fcrackzip -b -l 5 -c '1' -p 12345 <FileZip>
```

#### Proporcionar contraseña inicial
```
fcrackzip -b -c 'a' -p hola -u <FileZip>
```

#### Prueba de rendimiento
```
frackzip -B
```

#### Cambiar el método de romper la contraseña
```
frackzip -b -c 'a' -m 1 -u <FileZip>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)