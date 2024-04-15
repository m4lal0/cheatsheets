# ffuf Cheat Sheet

#### Fuzzing web usando una WORDLIST
```
ffuf -c -w <WORDLIST> -u http://target/FUZZ
```

#### Fuzzing web con recursividad
```
ffuf -c -w <WORDLIST> -recursion -recursion-depth 2 -u http://target/FUZZ
```

#### Fuzzing web con más velocidad modificando el número de hilos a usar
```
ffuf -c -w <WORDLIST> -t 60 -u http://target/FUZZ
```

#### Fuzzing web e ignorar los comentarios de la wordlists
```
ffuf -c -ic -w <WORDLIST> -u http://target/FUZZ
```

#### Descubrir archivos con extensiones
```
ffuf -c -w <WORDLIST> -e php,txt,sh,zip,html,bak,cgi,sql,old,git,js,bin,pl -u http://target/FUZZ
```

#### Fuzzing web y filtrando solamente páginas con código 200 y 301
```
ffuf -c -w <WORDLIST> -mc 200,301 -u http://target/FUZZ
```

#### Fuzzing web y no mostrar páginas con código 404
```
ffuf -c -w <WORDLIST> -fc 404 -u http://target/FUZZ
```

#### Fuzzing web, filtrando solamente páginas con código 200 y 301 y realizando follow redirects
```
ffuf -c -w <WORDLIST> -mc 200,301 -r -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo html
```
ffuf -c -w <WORDLIST> -o <OUTPUT> -of html -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo md
```
ffuf -c -w <WORDLIST> -o <OUTPUT> -of md -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo JSON
```
ffuf -c -w <WORDLIST> -o <OUTPUT> -u http://target/FUZZ
```

#### Fuzzing web usando una Cookie
```
ffuf -c -w <WORDLIST> -b <COOKIE> -u http://target/FUZZ
```

#### Fuzzing a cookies
```
ffuf -c -w <WORDLIST-SESSIONS> -b PHPSESSID=FUZZ -u http://target/
```

#### Enumeración de subdominios
```
ffuf -c -w <WORDLIST> -H "Host: FUZZ.target" -u http://target/ -fw18 -r

ffuf -c -w <WORDLIST> -u "http://FUZZ.target"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)