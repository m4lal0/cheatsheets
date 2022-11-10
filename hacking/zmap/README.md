# Zmap Cheat Sheet

#### Archivos de configuración
```
/etc/zmap/blacklist.conf
/etc/zmap/zmap.conf
```

#### Escanear un rango de IP's internas dentro de un archivo de lista blanca, al puerto 139, guardar el resultado
```
zmap -w <WHITELIST_FILE> -p 139 -o <OUTPUT_FILE> -v 5 -G <MAC-ADDRESS>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)