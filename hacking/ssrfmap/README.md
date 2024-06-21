# SSRFmap Cheat Sheet

#### Escaneo de la vulnerabilidad SSRF a un requeset con parametro llamado 'q' y revisar que puertos tiene abiertos localmente:
```
ssrfmap -r <REQUEST> -p q -m portscan
```

#### Escaneo de la vulnerabilidad SSRF a un requeset con parametro llamado 'q' y leer archivos localmente:
```
ssrfmap -r <REQUEST> -p q -m readfiles
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)