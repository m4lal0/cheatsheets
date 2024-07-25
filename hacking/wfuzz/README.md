# Wfuzz Cheat Sheet

### File Discovery

#### Fuzzing a sitio web quitando código 404
```
wfuzz -c -t 400 --hc=404 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Usar Follow redirect para códigos 301
```
wfuzz -c -L -t 400 --hc=404 -w /Directorio/de/Wordlist http://Target/FUZZ
```

#### Usar Follow redirect para códigos 301 y guardar los resultado
```
wfuzz -c -L -t 400 --hc=404 -f <OUTPUT> -w /Directorio/de/Wordlist http://Target/FUZZ
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

#### Cambiar User-Agent
```
wfuzz -c -H " User-Agent: Google Chrome" -t 400 --hc=404 -w /Directorio/de/Wordlist http://target/FUZZ
```

#### Fuzzing para plugins WordPress
```
wfuzz -c -t 200 --hc=404 -w /usr/share/wordlists/seclists/Discovery/Web-Content/CMS/wp-plugins.fuzz.txt http://target/FUZZ
```

#### Fuzzing recursivo y solo mostrando sitios con código de respuesta 200 y 301
```
wfuzz -c -w /Directorio/de/Wordlist -R 3 --sc 301,200 http://target/FUZZ
```

### Directory Discovery

#### Busqueda de directorios y ocultando los resultados con codigo 404 y 301
```
wfuzz -c -z file,/usr/share/wordlists/seclists/Discovery/Web-Content/raft-large-directories.txt --hc 404,301 "<URL>/FUZZ/"
```

### Parameter Discovery

#### Fuzzing párametros en un directorio del sitio web
```
wfuzz -c -t 200 --hc=404 -H "Cookie: PHPSESSID=Value" -w /usr/share/wordlists/seclists/Discovery/Web-Content/burp-parameter-names.txt http://target/dir?FUZZ=
```

#### Fuzzing de parametros
```
wfuzz -c -z file,/usr/share/wordlists/seclists/Discovery/Web-Content/burp-parameter-names.txt --hc 404,301 "<URL>/FUZZ=data"
```

### Fuzzing Parameter Values

#### Busqueda de Valores en un parametro
```
wfuzz -c --hh=40060 -z file,/usr/share/wordlists/seclists/Fuzzing/XSS-Fuzzing --hc 404,301 "<URL>/?xss=FUZZ"
```

### Fuzzing POST Data

#### Fuzzing en Formulario
```
wfuzz -c --h=429 -w /Directorio/de/Wordlist -d 'usuario=FUZZ&password=test' http://target/login.php
```

#### Fuzzing en Formulario, no mostrando resultado con el mensaje de error al no encontrar el usuario
```
wfuzz -c --hs "No account found with that username." -w /Directorio/de/Wordlist -d 'usuario=FUZZ&password=test' http://target/login.php
```

#### Fuzzing SSRF
```
wfuzz -c -z range,1-65535 -d 'formurl=http://localhost:FUZZ+-s&sumbit=Go' http://target/exposed.php
```

### Fuzzing Cookies

#### Fuzzing a Cookie
```
wfuzz -c -w /Directorio/de/Wordlist-Sessions -b PHPSESSID=FUZZ http://target/
```

### Subdomains Discovery

#### Enumerar subdominios
```
wfuzz -c -t 200 --hc=301 -w /usr/share/wordlists/seclists/Directory/DNS/subdomains-top1million-110000.tx -H "Host: FUZZ.target" http://target
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)