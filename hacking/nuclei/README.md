# Nuclei Cheat Sheet

#### Escanear un sitio web
```
nuclei -u <Target>
```

#### Escanear un sitio web usando plantillas de CVEs y Exposures
```
nuclei -u <Target> -t cves/ -t exposures/
```

#### Escanear un sitio web y guardar los resultados en un archivo
```
nuclei -u <Target> -o <Output>
```

#### Escanear un sitio web y guardar los resultados en un archivo JSON
```
nuclei -u <Target> -json <Output>
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