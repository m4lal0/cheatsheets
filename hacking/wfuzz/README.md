# Wfuzz Cheat Sheet

#### Fuzzing a sitio web quitando código 404
```
wfuzz -c -t 400 --hc=404 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Usar Follow redirect para códigos 301
```
wfuzz -c -L -t 400 --hc=404 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Mostrar directorios con código 200
```
wfuzz -c -t 400 --sc=200 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Mostrar directorios que tengan un cierto número de carácteres
```
wfuzz -c -t 400 --sh=2385 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Ocultar el número de líneas de un directorio
```
wfuzz -c -t 400 --hl=170 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Doble Payload para Fuzzing
```
wfuzz -c -t 400 --hc=404 -w /Directorio/de/Wordlist -w extensions.txt http://target/FUZZ.FUZ2Z
```

#### Cambiar User-Agent
```
wfuzz -c -H " User-Agent: Google Chrome" -t 400 --hc=404 -w /Directorio/de/Wordlist http://target/FUZZ
```

#### Fuzzing en Formulario
```
wfuzz -c --h=429 -w /Directorio/de/Wordlist -d 'usuario=FUZZ&password=test' http://target/login.php
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)