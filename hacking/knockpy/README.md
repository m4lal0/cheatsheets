# Knockpy Cheat Sheet

#### Escaneo de subdominios usando una WordList
```
knockpy -d <DOMAIN> --wordlist <WORDLIST> --bruteforce
```

#### Escaneo de subdominios leyendo los dominios desde un archivo
```
knockpy -f <FILE-NAME> --wordlist <WORDLIST> --bruteforce
```

#### Escaneo y reconocimiento de subdominios usando una WordList
```
knockpy -d <DOMAIN> --wordlist <WORDLIST> --bruteforce --recon
```

#### Escaneo de subdominios y guardar el resultado en un directorio dado
```
knockpy -d <DOMAIN> --wordlist <WORDLIST> --bruteforce --save <DIRECTORY-NAME>
```

#### Mostrar el resultado de un reporte de knockpy
```
knockpy --report <REPORT-NAME.json>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)