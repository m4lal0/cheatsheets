# raven Cheat Sheet

#### Crear un webserver en el directorio actual y en un puerto dado
```
raven 0.0.0.0 <LISTENING-PORT>
```

#### Webserver y solo permitir a una cierta dirección IP el acceso
```
reaven <LISTENING-IP> <LISTENING-PORT> --allowed-ip <IP>
```

#### Webserver y permitir subir archivos en un directorio dado (/tmp)
```
reaven <LISTENING-IP> <LISTENING-PORT> --upload-folder /tmp
```

#### Webserver, permitir subir archivos en un directorio dado y organizar por IP los archivos
```
reaven <LISTENING-IP> <LISTENING-PORT> --upload-folder /tmp --organize-uploads
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)