# DalFox Cheat Sheet

#### Escaneo simple para buscar vulnerabilidades XSS
```
dalfox url <URL>
```

#### Escaneo a multiples URLs que estan un archivo
```
dalfox file <URLS_FILE>
```

#### Escaneo a un Request como de Burp/Zap
```
dalfox file <RAWDATA_FILE> --rawdata
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

#### Escaneo y generar un informe detallado
```
dalfox url <URL> --report -o <OUTPUT>
```

#### Escaneo solamente de XSS y desactivar el escaneo de otras vulnerabilidades (SQLi, SSTI, Open Redirect, CRLF injection)
```
dalfox url <URL> --skip-bav
```

#### Escaneo de otras vulnerabilidades (SQLi, SSTI, Open Redirect, CRLF injection)
```
dalfox url <URL> --use-bav
```

#### Escaneo y evadir WAF
```
dalfox url <URL> --waf-evasion
```

#### Escaneo y usar una wordlist
```
dalfox url <URL> --mining-dict-word=<WORDLIST_PATH>
```

#### Escaneo y usar payloads remotos
```
dalfox url <URL> --remote-payloads portswigger,payloadbox
```

#### Escaneo con método POST
```
dalfox url <URL> --waf-evasion -X POST -d "email=test&pwd=test" -p <PARAMETER>
```

#### Escaneo, haciendo un follow redirect y enviar los request a un proxy
```
dalfox url <URL> --proxy http://127.0.0.1:8080 -F
```

#### Escaneo XSS desde una linea
```
gospider -s <URL> -c 10 -d 5 --blacklist ".(jpg|jpeg|gif|css|tif|tiff|png|ttf|woff|woff2|ico|pdf|svg|txt)" --other-source | grep -e "code-200" | awk '{print $5}'| grep "=" | qsreplace -a | dalfox pipe | tee result.txt
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)