# Waybackurls Cheat Sheet

#### Crawling a un sitio web
```
waybackurls <DOMAIN>
```

#### Crawling sólo al dominio principal, no se tiene en cuenta los subdominios a rastrear
```
echo "DOMAIN" | waybackurls -no-subs
```

#### Crawling al sitio web y mostrar las fechas obtenidas en wayback en la primera columna
```
echo "DOMAIN" | waybackurls -dates
```

#### Crawling al sitio web y mostrar la URL de wayback para explorar mas sobre ello
```
echo "DOMAIN" | waybackurls -get-versions
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)