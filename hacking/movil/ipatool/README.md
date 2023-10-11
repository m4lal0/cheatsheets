# IPAtool Cheat Sheet

#### Autenticarse para usar la herramienta
```
ipatool auth login -e '<USER> -p '<PASSWORD>'
```

#### Buscar el aplicativo y obtener el ID
```
ipatool search --limit 1 <APP-NAME>
```

#### Obtener la licencia para descargar el aplicativo
```
ipatool purchase -b <ID-APP-BUNDLE>
```

#### Descargar el IPA de la aplicación
```
ipatool download --bundle-identifier <ID-APP-BUNDLE> --output <OUTPUT-NAME>.ipa
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)