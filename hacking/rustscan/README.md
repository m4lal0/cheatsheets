# RustScan Cheat Sheet

#### Obtener todos los puertos abiertos del objetivo (3000 puertos por segundo)
```
rustscan -a <IP-ADDRESS>
```

#### Mostrar solo los puertos abiertos en modo grepeable
```
rustscan -a <IP-ADDRESS> -u 5000 -g
```

#### Obtener todos los puertos abiertos, la cantidad de puertos analizados por segundo sea de 500 y el limite de archivo sea de 5000
```
rustscan -b 500 -a <IP-ADDRESS> -u 5000
```

#### Usar flags de Nmap
```
rustscan -b 500 -a <IP-ADDRESS> -u 5000 -- -sC -sV
```

#### Devolver el resultado del escaneo en un formato que podamos filtrar con grep
```
rustscan -g -a <IP-ADDRESS>
```

#### Especificar puertos a escanear
```
rustscan -a <IP-ADDRESS> -p 80,443,8080,21
```

#### Especificar un rango de puertos a escanear
```
rustscan -a <IP-ADDRESS> -r 1-1000
```

#### Escanear puertos y solo mostrar resultados sin banner y letras ASCII 
```
rustscan -a <IP-ADDRESS> --accessible
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)