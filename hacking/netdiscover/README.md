# NetDiscover Cheat Sheet

#### Uso básico de escaneo
```
netdiscover -i <Interface>
```

#### Escanear especificando un rango de IP
```
netdiscover -r 192.168.6.0/24,/16,/8
```

#### Escanear desde un archivo con listado de rangos
```
netdiscover -l <File>
```

#### Escaneo en modo pasivo
```
netdiscover -i <Interface> -p
```

#### Mostrar el escaneo en modo Parsable y no mostrar los encabezados
```
netdiscover -i <Interface> -PN
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)