# CeWL Cheat Sheet

#### Rastrear un sitio y escribir todas las palabras encontradas en un archivo
```
cewl <url> -w <file>
```

#### Crear un archivo de palabras de un sitio con una profundidad determinada y una longitud mínima de palabras
```
cewl <url> -d <depth> -m <min-word-length> -w <file>
```

#### Rastrear un sitio y seguir enlaces a otros sitios
```
cewl <url> -o
```

#### Spider a un sitio usando un user-agent determinado
```
cewl <url> -u <user-agent>
```

#### Spider a un sitio e incluir un recuento de cada palabra
```
cewl <url> -c
```

#### Spider a un sitio que incluya metadatos y separar las palabras de meta_datos
```
cewl <url> -a -meta_file -w <file>
```

#### Spider a un sitio y almacenar direcciones de correo electrónico en un archivo separado
```
cewl <url> -e -email_file -w <file>
```

#### Generar una lista de palabras alfanúmericas
```
cewl <url> --with-numbers
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)