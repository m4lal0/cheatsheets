# URLBuster Cheat Sheet

#### Fuzzing web usando una Wordlist
```
urlbuster -W <Wordlist> <URL>
```

#### Fuzzing web a sitio HTTPS y usando una Wordlist
```
urlbuster -W <Wordlist> -k <URL>
```

#### Fuzzing web guardando el resultado en un archivo
```
urlbuster -W <Wordlist> --output <Output> <URL>
```

#### Fuzzing web usando una autenticación básica
```
urlbuster -W <Wordlist> --auth-basic '<user>:<pass>' <URL>
```

#### Fuzzing web usando una Cookie session
```
urlbuster -W <Wordlist> --cookie '<Cookie>' <URL>
```

#### Fuzzing web que solo muestre directorios o archivos con codigos de estatus en especifico
```
urlbuster -W <Wordlist> --code 200 301 302 <URL>
```

#### Fuzzing web que muestre estatus de codigos en concretos y realice follow redirects
```
urlbuster -W <Wordlist> --code 200 301 302 --follow <URL>
```

#### Fuzzing web buscando archivos con extensiones en especifico
```
urlbuster -W <Wordlist> --code 200 301 302 --ext .zip .tar .tar.gz .gz .rar <URL>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)