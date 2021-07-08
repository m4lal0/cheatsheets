# FeroxBuster Cheat Sheet

### Fuzzing web y guardar resultado en un archivo
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -o <Output>
```

### Fuzzing web con follow redirect y no mostrar códigos en 404 y 403
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -C 404,403 -r -o <Output>
```

### Fuzzing web por extensiones de archivos
```
feroxbuster -u <URL> -w <Wordlist> -t <Threads> -x php txt js pdf -o <Output>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)