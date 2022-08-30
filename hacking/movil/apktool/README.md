# APKTool Cheat Sheet

#### Decodificar.
```
apktool d example.apk
```

#### Evitar que el archivo classes.dex sea desensamblado.
```
apktool d -s example.apk
```

#### Decodificar y eliminar si existe el directorio.
```
apktool d example.apk -f
```

#### Re-empacar una aplicación.
```
apktool b Directroio_Aplicacion/ -o NewName.apk
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)