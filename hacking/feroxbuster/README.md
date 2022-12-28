# FeroxBuster Cheat Sheet

### Fuzzing web y guardar resultado en un archivo
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -o <Output>
```

### Fuzzing web con follow redirect y no mostrar códigos en 404 y 500, con profundidad de 2
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -C 404,500 -r --depth 2 -o <Output>
```

### Fuzzing web con follow redirect y mostrar solo con código en 200 y 301
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -s 200,301 -r -o <Output>
```

### Fuzzing web por extensiones de archivos
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -x php txt js pdf -o <Output>
```

### Fuzzing web cambiando el Headers
```
feroxbuster -u <URL> -w <Wordlist> -H Accept:application/json "Authorization: Bearer {token}"
```

### Fuzzing web a través de un proxy SOCKS
```
feroxbuster -u <URL> -w <Wordlist> --proxy socks5://127.0.0.1:9050
```

### Fuzzing web a través del proxy Burp
```
feroxbuster -u <URL> -w <Wordlist> --insecure --proxy http://127.0.0.1:8080
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)