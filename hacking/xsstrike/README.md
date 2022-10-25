# XSStrike Cheat Sheet

#### Escaneo a un sitio usando metodo GET
```
xsstrike.py -u "<URL>"
```

#### Escaneo a un sitio usando metodo POST
```
xsstrike.py -u "<URL>" --data "q=query"
```

#### Escaneo a un sitio usando metodo POST con datos JSON
```
xsstrike.py -u "<URL>" --data '{"q":"query"}' --json
```

#### Brute force desde un archivo
```
xsstrike.py -u "<URL>" -f <PATH_FILE>
```

#### Blind XSS
```
xsstrike.py -u "<URL>" --crawl --blind
```

#### Payloads codificadas en Base64
```
xsstrike.py -u "<URL>" -e base64
```

#### Fuzzing
```
xsstrike.py -u "<URL>" --fuzzer
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)