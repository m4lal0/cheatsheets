# Masscan command Cheat Sheet

#### Escaneo general
```
masscan 192.168.1.0/24
```

#### Escaneo general excluyendo una IP
```
masscan 192.168.1.0/24 --exclude=192.168.1.15
```

#### Escaneo general especificando puertos TCP
```
masscan 192.168.1.10 -p 0-65535
masscan 192.168.1.10 -p 21,80,443
```

#### Escaneo de puertos abiertos a una IP
```
masscan 192.168.1.10 -p 0-65535 --rate 10000 --open-only
```

#### Escaneo general especificando puertos UDP
```
masscan 192.168.1.10 -pU 53
```

#### Escaneo general usando una tasa de envio de paquetes por segundo
```
masscan 192.168.1.0/24 --rate 5000
```

#### Escaneo general y guardar el resultado en formato simple
```
masscan 192.168.1.0/24 -oL <OUTPUT>
```

#### Opciones para guardar resultados
```
-oB : Modo binario
-oX : Formato XML
-oG : Formato grepeable
-oJ : Formato JSON
-oL : Formato listado simple
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)