# DNSMap Cheat Sheet

#### Enumerar sub-dominios
```
dnsmap <Domain>
```

#### Enumerar sub-dominios usando una Wordlist
```
dnsmap <Domain> -w <Wordlist>
```

#### Enumerar sub-dominios y guardar los resultados
```
dnsmap <Domain> -r </path/output>
```

#### Enumerar sub-dominios y guardar los resultados en formato CSV
```
dnsmap <Domain> -c -r </path/output>
```

#### Enumerar sub-dominios pero ignorando unas direcciones IP's
```
dnsmap <Domain> -w <Wordlist> -i 10.55.206.154,10.55.24.100
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)