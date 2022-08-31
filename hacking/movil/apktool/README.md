# APKTool Cheat Sheet

#### Decodificar.
```
apktool d example.apk
```

#### Decodificar y guardar con nombre personalizado.
```
apktool d example.apk -o Output
```

#### Decodificar y evitar que el archivo classes.dex sea desensamblado.
```
apktool d -s example.apk
```

#### Decodificar y eliminar si existe el directorio.
```
apktool d -f example.apk
```

#### Decodificar y mantener el archivo resources.arsc sin decodificación para sólo editar smali.
```
apktool d -r example.apk
```

#### Re-empacar una aplicación y guardar con nombre personalizado.
```
apktool b Directroio_Aplicacion/ -o NewName.apk
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)