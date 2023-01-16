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

#### Doble Payload para Fuzzing de extensiones, especificando las extensiones a buscar (sh,pl,cgi)
```
wfuzz -c -t 200 --hc=404 -w /Directorio/de/Wordlist -z list,sh-pl-cgi http://target/FUZZ.FUZ2Z
```

#### Fuzzing a Cookie
```
wfuzz -c -w /Directorio/de/Wordlist-Sessions -b PHPSESSID=FUZZ http://target/
```

#### Cambiar User-Agent
```
wfuzz -c -H " User-Agent: Google Chrome" -t 400 --hc=404 -w /Directorio/de/Wordlist http://target/FUZZ
```

#### Fuzzing en Formulario
```
wfuzz -c --h=429 -w /Directorio/de/Wordlist -d 'usuario=FUZZ&password=test' http://target/login.php
```

#### Enumerar subdominios
```
wfuzz -c -t 200 -w /usr/share/seclists/Directory/DNS/subdomains-top1million-5000.txt -H "Host: FUZZ.target" http://target
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)