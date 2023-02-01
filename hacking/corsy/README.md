# Corsy Cheat Sheet

#### Auditar CORS a un sitio web
```
corsy -u <URL>
```

#### Auditar varios sitios web de CORS desde un archivo
```
corsy -i <PATH-TO-FILE>
```

#### Auditar CORS a un sitio web y guardar el resultado en JSON
```
corsy -u <URL> -o <OUTPUT.json>
```

#### Auditar CORS a un sitio web y colocando un delay entre cada petición
```
corsy -u <URL> -d 2
```

#### Auditar CORS a un sitio web y agregando un encabezado personalizado
```
corsy -u <URL> --headers "User-Agent: GoogleBot\nCookie: SESSION=Hacked"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)