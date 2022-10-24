# DalFox Cheat Sheet

#### Escaneo simple para buscar vulnerabilidades XSS
```
dalfox url <URL>
```

#### Escaneo multiple leyendo un archivo de objetivos
```
dalfox file <URLS_FILE>
```

#### Escaneo y guardar los resultados
```
dalfox url <URL> -o <OUTPUT>
```

#### Escaneo y guardar solamente los resultados con codigo 'grep (g)' y 'verified (v)'
```
dalfox url <URL> --only-poc=g,v

g(grep)
r(reflected)
v(verified)
```

#### Escaneo de XSS y otras vulnerabilidades (SQLi, SSTI, Open Redirect, CRLF injection)
```
dalfox url <URL> --skip-bav
```

#### Escaneo y usar una wordlist
```
dalfox url <URL> --mining-dict-word=<WORDLIST_PATH>
```

#### Escaneo y usar payloads remotos
```
dalfox url <URL> --remote-payloads portswigger,payloadbox
```

#### Escaneo XSS desde una linea
```
gospider -s <URL> -c 10 -d 5 --blacklist ".(jpg|jpeg|gif|css|tif|tiff|png|ttf|woff|woff2|ico|pdf|svg|txt)" --other-source | grep -e "code-200" | awk '{print $5}'| grep "=" | qsreplace -a | dalfox pipe | tee result.txt
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)