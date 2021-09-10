# ffuf Cheat Sheet

#### Fuzzing web usando una Wordlist
```
ffuf -w <Wordlist> -u http://target/FUZZ
```

#### Fuzzing web con recursividad
```
ffuf -w <Wordlist> -recursion -u http://target/FUZZ
```

#### Fuzzing web con más velocidad modificando el número de hilos a usar
```
ffuf -w <Wordlist> -t 60 -u http://target/FUZZ
```

#### Descubrir archivos con extensiones
```
ffuf -w <Wordlist> -e .log,.txt,.php -u http://target/FUZZ
```

#### Fuzzing web y filtrando solamente páginas con código 200 y 301
```
ffuf -w <Wordlist> -mc 200,301 -u http://target/FUZZ
```

#### Fuzzing web, filtrando solamente páginas con código 200 y 301 y realizando follow redirects
```
ffuf -w <Wordlist> -mc 200,301 -r -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo html
```
ffuf -w <Wordlist> -o <Output> -of html -u http://target/FUZZ
```

#### Fuzzing web y guardar el resultado en un archivo JSON
```
ffuf -w <Wordlist> -o <Output> -u http://target/FUZZ
```

#### Fuzzing web usando una Cookie
```
ffuf -w <Wordlist> -b <Cookie> -u http://target/FUZZ
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)