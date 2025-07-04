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
ffuf -c -ic -w <WORDLIST> -e .php,.txt,.sh,.zip,.html,.bak,.cgi,.sql,.old,.git,.js,.bin,.pl -u http://target/FUZZ
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
ffuf -c -ic -w <WORDLIST> -mc 200,301,302,401,500 -r -fs 0 -u http://target/FUZZ
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

#### Fuzzing de extensiones
```
ffuf -c -ic -w /usr/share/seclists/Discovery/Web-Content/web-extensiones.txt -u "http://<URL>/indexFUZZ"
```

#### Fuzzing a parametros GET
```
ffuf -c -ic -w /usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt -u "http://<URL>/index.php?FUZZ=data" -fs 0
```

#### Fuzzing a parametros POST
```
ffuf -w /opt/useful/SecLists/Discovery/Web-Content/burp-parameter-names.txt -u http://<URL>:<PORT>/admin/admin.php -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' -b "PHPSESSID=hpuqc6h0nc7jbcbtnkish21di8" -fs xxx
```

#### Fuzzing a parametros POST y filtrando por un mensaje de error
```
ffuf -w /opt/useful/SecLists/Discovery/Web-Content/burp-parameter-names.txt -u http://<URL>:<PORT>/admin/admin.php -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' -fr "Unknown user"
```

#### Fuzzing a Login POST usando un request de Burp y encontrar usuarios validos
```
ffuf -request request.txt -fw 10 -request-proto http -mode pitchfork -w /usr/share/wordlists/seclists/Usernames/Names/names.txt:USERFUZZ -mc 200
```

#### Fuzzing Subdominios - DNS
```
ffuf -c -ic -w <WORDLIST> -u "http://FUZZ.target"
```

#### Enumeración de subdominios - VHost
```
ffuf -c -ic -w <WORDLIST> -H "Host: FUZZ.target" -u http://target/ -r
```

#### Fuzzing web y enviar todo el tráfico a un proxy web
```
ffuf -c -u http://target/FUZZ -w <WORDLIST> -x http://127.0.0.1:8080
ffuf -c -u http://target/FUZZ -w <WORDLIST> -replay-proxy http://127.0.0.1:8080
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)