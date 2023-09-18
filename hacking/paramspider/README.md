# Paramspider Cheat Sheet

#### Simple escaneo
```
paramspider.py --domain <DOMAIN>
```

#### Excluir extensiones específicas
```
paramspider.py --domain <DOMAIN> --exclude woff,css,png,svg,jpg,gif,jpeg,swf
```

#### Encontrar parámetros anidados
```
paramspider.py --domain <DOMAIN> --level high
```

#### Guardar los resultados
```
paramspider.py --domain <DOMAIN> --exclude woff,css,png,svg,jpg,gif,jpeg,swf --level high --output <OUTPUT>.txt
```

#### Usar modo silencioso (No imprimir las URLs en pantalla)
```
paramspider.py --domain <DOMAIN> --exclude woff,css,png,svg,jpg,gif,jpeg,swf --level high --output <OUTPUT>.txt --quiet
```

#### Excluir subdominios
```
paramspider.py --domain <DOMAIN> --subs False
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)