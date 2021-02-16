# DNSEnum Cheat Sheet

#### Enumerar los DNS de un dominio
```
dnsenum --enum <Domain>
```

#### Enumerar los DNS de un dominio y guardar el resultado en un archivo XML
```
dnsenum --enum <Domain> --output <File>
```

#### Enumerar dominios usando Bruteforce desde una lista de un archivo
```
dnsenum -f <FileSubdomain> -r <Domain>
```

#### Guardar todos los subdominios validos en un archivo
```
dnsenum <domain> --subfile <File>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)