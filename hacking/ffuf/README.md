# ffuf Cheat Sheet

#### Fuzzing web usando una WORDLIST
```
ffuf -c -w <WORDLIST> -u http://target/FUZZ
```

#### Fuzzing web e ignorar los comentarios de la wordlists
```
ffuf -c -ic -w <WORDLIST> -u http://target/FUZZ
```

#### Fuzzing web con recursividad
```
ffuf -c -ic -w <WORDLIST> -recursion -recursion-depth 2 -u http://target/FUZZ
```

#### Fuzzing web con más velocidad modificando el número de hilos a usar
```
ffuf -c -ic -w <WORDLIST> -t 60 -u http://target/FUZZ
```

#### Descubrir archivos con extensiones
```
ffuf -c -ic -w <WORDLIST> -e php,txt,sh,zip,html,bak,cgi,sql,old,git,js,bin,pl -u http://target/FUZZ
```

#### Fuzzing web y filtrando solamente páginas con código 200,301,302,401 y 500
```
ffuf -c -ic -w <WORDLIST> -mc 200,301,302,401,500 -u http://target/FUZZ
```

#### Fuzzing web y no mostrar páginas con código 404
```
ffuf -c -ic -w <WORDLIST> -fc 404 -u http://target/FUZZ
```

#### Fuzzing web, filtrando solamente páginas con código 200 y 301 y realizando follow redirects
```
ffuf -c -ic -w <WORDLIST> -mc 200,301 -r -u http://target/FUZZ
```

#### Fuzzing web, mostrando sitios con código 200,301,302,401 y 500, y quitando de los resultados los que tengan de tamaño 0
```
ffuf -c-ic -w <WORDLIST> -mc 200,301,302,401,500 -r -fs 0 -u http://target/FUZZ
```

#### Fuzzing web y filtrando solamente páginas que no tengan de salida de Words (Palabras) 39
```
ffuf -c -ic -w <WORDLIST> -fw 39 -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo html
```
ffuf -c -ic -w <WORDLIST> -o <OUTPUT> -of html -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo md
```
ffuf -c -ic -w <WORDLIST> -o <OUTPUT> -of md -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo JSON
```
ffuf -c -ic -w <WORDLIST> -o <OUTPUT> -u http://target/FUZZ
```

#### Fuzzing web usando una Cookie
```
ffuf -c -ic -w <WORDLIST> -b <COOKIE> -u http://target/FUZZ
```

#### Fuzzing a cookies
```
ffuf -c -ic -w <WORDLIST-SESSIONS> -b PHPSESSID=FUZZ -u http://target/
```

#### Fuzzing de numeros usando la salida de un comando (STDIN)
```
for i in {0..255}; do echo $i; done | ffuf -c -u 'http://target/?id=FUZZ' -w -
```

#### Enumeración de subdominios - VHost
```
ffuf -c -ic -w <WORDLIST> -H "Host: FUZZ.target" -u http://target/ -fs 0 -r

ffuf -c -ic -w <WORDLIST> -u "http://FUZZ.target" -fs 0
```

#### Fuzzing web y enviar todo el tráfico a un proxy web
```
ffuf -c -u http://target/FUZZ -w <WORDLIST> -x http://127.0.0.1:8080
ffuf -c -u http://target/FUZZ -w <WORDLIST> -replay-proxy http://127.0.0.1:8080
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)