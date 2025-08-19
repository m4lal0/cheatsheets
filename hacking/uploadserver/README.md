# uploadserver Cheat Sheet

#### Crear un webserver en el puerto por default (8000)
```
python3 -m uploadserver
```

#### Crear un webserver en otro puerto especificado
```
python3 -m uploadserver <PORT>
```

#### Crear un webserver en el puerto por default con autenticación básica
```
python3 -m uploadserver --basic-auth <USER>:<PASSWORD>
```

#### Crear un webserver en el puerto por default con autenticación básica solo para cargar archivos
```
python3 -m uploadserver --basic-auth-upload <USER>:<PASSWORD>
```

#### Crear un webserver en el puerto por default usando tema dark o light
```
python3 -m uploadserver --theme light

python3 -m uploadserver --theme dark
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)