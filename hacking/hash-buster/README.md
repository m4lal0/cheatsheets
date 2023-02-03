# Hash-Buster Cheat Sheet

#### Crackear un hash (Soporta MD5, SHA1, SHA256, SHA384, SHA512)
```
hash-buster -s <HASH>
```

#### Buscar directorios que contengan hashes y crackearlos
```
hash-buster -d /root/Documents
```

#### Crackear hashes desde un archivo dado
```
hash-buster -f <FILE>
```

#### Crackear hashes desde un archivo dado y haciendo varias peticiones en paralelo
```
hash-buster -f <FILE> -t 10
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)