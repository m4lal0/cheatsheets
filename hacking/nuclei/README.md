# Nuclei Cheat Sheet

#### Escanear un sitio web
```
nuclei -u <TARGET>
```

#### Escanear un sitio web y muestra solamente las trazas
```
nuclei -u <TARGET> -silent
```

#### Escanear una lista de sitios web desde un archivo
```
nuclei -l <FILE-TARGETS>
```

#### Escanear un sitio web usando plantillas de CVEs y Exposures
```
nuclei -u <TARGET> -t cves/ -t exposures/
```

#### Escanear un sitio web usando plantillas y diferentes severidades
```
nuclei -u <Target> -t cves/ -t vulnerabilities -severity critical,high,medium
```

#### Escanear un sitio web y excluir tags
```
nuclei -u <TARGET> -etags sqli,xss,rce
```

#### Escanear un sitio web y guardar los resultados en un archivo
```
nuclei -u <TARGET> -o <Output>
```

#### Escanear un sitio web y guardar los resultados en un archivo JSON
```
nuclei -u <TARGET> -json <Output>
```

#### Actualizar plantillas
```
nuclei -ut
```

#### Actualizar nuclei
```
nuclei -update
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)