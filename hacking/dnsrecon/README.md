# DNSRecon Cheat Sheet

#### Enumerar los DNS de un dominio
```
dnsrecon -d <Domain>
```

#### Enumerar los DNS de un dominio y guardar el resultado en una BD SQLite
```
dnsrecon -d <Domain> -db /path/to/sqllite.file
```

#### Enumerar subdominios por fuerza bruta
```
dnsrecon -d <Domain> -n <DNS-Domain> -D /path/to/Wordlist -t brt
```

#### Utilizar Google para la búsqueda de host y dominios
```
dnsrecon -d <Domain> -n <DNS-Domain> -t goo
```

#### DNSSEC Zone Walking
```
dnsrecon -d <Domain> -z
```

#### Transferencia de Zona
```
dnsrecon -d <Domain> -t axfr
```

#### Reverse Lookup
```
dnsrecon -r 208.67.222.200-208.67.222.255 -d microsoft.com
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)