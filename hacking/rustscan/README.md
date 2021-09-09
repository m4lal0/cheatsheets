# RustScan Cheat Sheet

#### Obtener todos los puertos abiertos del objetivo (3000 puertos por segundo)
```
rustscan -a <IP-Address>
```

#### Obtener todos los puertos abiertos, la cantidad de puertos analizados por segundo sea de 500 y el limite de archivo sea de 5000
```
rustscan -b 500 -a <IP-Address> -u 5000
```

#### Usar flags de Nmap
```
rustscan -b 500 -a <IP-Address> -u 5000 -- -sC -sV
```

#### Devolver el resultado del escaneo en un formato que podamos filtrar con grep
```
rustscan -g -a <IP-Address>
```

#### Especificar puertos a escanear
```
rustscan -a <IP-Address> -p 80,443,8080,21
```

#### Especificar un rango de puertos a escanear
```
rustscan -a <IP-Address> -r 1-1000
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)