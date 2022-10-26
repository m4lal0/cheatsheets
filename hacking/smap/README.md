# Smap Cheat Sheet

#### Escaneo de una IP pública
```
smap <IP>
```

#### Escaneo a un listado de Hosts
```
smap -iL <FILE>
```

#### Escaneo y guardar el resultado en XML
```
smap <IP> -oX <OUTPUT>
```

#### Formatos para guardar soportados
```
-oX : nmap's xml format
-oG : nmap's greppable format
-oN : nmap's default format
-oA : output in all 3 formats above at once
-oP : IP:PORT pairs seperated by newlines
-oS : custom smap format
-oJ : json
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)