# ffuf Cheat Sheet

#### Fuzzing web usando una Wordlist
```
ffuf -c -w <Wordlist> -u http://target/FUZZ
```

#### Fuzzing web con recursividad
```
ffuf -c -w <Wordlist> -recursion -u http://target/FUZZ
```

#### Fuzzing web con más velocidad modificando el número de hilos a usar
```
ffuf -c -w <Wordlist> -t 60 -u http://target/FUZZ
```

#### Descubrir archivos con extensiones
```
ffuf -c -w <Wordlist> -e php,txt,sh,zip,html,bak,cgi,sql,old -u http://target/FUZZ
```

#### Fuzzing web y filtrando solamente páginas con código 200 y 301
```
ffuf -c -w <Wordlist> -mc 200,301 -u http://target/FUZZ
```

#### Fuzzing web, filtrando solamente páginas con código 200 y 301 y realizando follow redirects
```
ffuf -c -w <Wordlist> -mc 200,301 -r -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo html
```
ffuf -c -w <Wordlist> -o <Output> -of html -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo md
```
ffuf -c -w <Wordlist> -o <Output> -of md -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo JSON
```
ffuf -c -w <Wordlist> -o <Output> -u http://target/FUZZ
```

#### Fuzzing web usando una Cookie
```
ffuf -c -w <Wordlist> -b <Cookie> -u http://target/FUZZ
```

#### Fuzzing a cookies
```
ffuf -c -w <Wordlist-Sessions> -b PHPSESSID=FUZZ -u http://target/
```

#### Enumeración de subdominios
```
ffuf -c -w <Wordlist> -H "Host: FUZZ.target" -u http://target/ -fw18 -r

ffuf -c -w <Wordlist> -u "http://FUZZ.target"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)