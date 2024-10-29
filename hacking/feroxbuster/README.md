# FeroxBuster Cheat Sheet

### Fuzzing web y guardar resultado en un archivo
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -o <OUTPUT>
```

### Fuzzing web a un sitio con https y guardar el resultado en un archivo
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -o <OUTPUT> -k
```

### Fuzzing web con follow redirect y no mostrar códigos en 404 y 500, con profundidad de 2
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -C 404,500 -r --depth 2 -o <OUTPUT>
```

### Fuzzing web con follow redirect y no mostrar códigos en 404 y 500, con todas las profundidades de directorios.
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -C 404,500 -r --depth 0 -o <OUTPUT>
```

### Fuzzing web con follow redirect y no mostrar códigos en 404 y 500, con todas las profundidades de directorios y enviar los directorios al Burp Suite.
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -C 404,500 -r --depth 0 --burp-replay -o <OUTPUT>
```

### Fuzzing web con follow redirect y mostrar solo con código en 200 y 301
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -s 200,301 -r -o <OUTPUT>
```

### Fuzzing web por extensiones de archivos
```
feroxbuster -u <URL> -w <WORDLIST> -t <THREADS> -x txt php sh html sql js git bin -o <OUTPUT>
```

### Fuzzing web cambiando el Headers
```
feroxbuster -u <URL> -w <WORDLIST> -H Accept:application/json "Authorization: Bearer {token}"
```

### Fuzzing web a través de un proxy SOCKS
```
feroxbuster -u <URL> -w <WORDLIST> --proxy socks5://127.0.0.1:9050
```

### Fuzzing web a través del proxy Burp
```
feroxbuster -u <URL> -w <WORDLIST> --insecure --proxy http://127.0.0.1:8080
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)