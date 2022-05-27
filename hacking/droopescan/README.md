# DroopeScan Cheat Sheet

#### Obtener una lista completa y detalla de opciones de escaneo
```
droopescan scan --help
```

#### Escanear un sitio web y que se identifique el CMS
```
droopescan scan -u <URL-TARGET>
```

#### Escanear un listado de sitios webs y que se identifique el CMS
```
droopescan scan -U <FILE-OF-URLS>
```

#### Escanear un sitio web que usa WordPress
```
droopescan scan wordpress -u <URL-TARGET>
```

#### Escanear un sitio web que usa Drupal
```
droopescan scan drupal -u <URL-TARGET>
```

#### Escanear un sitio web que usa Joomla
```
droopescan scan joomla -u <URL-TARGET>
```

#### Escanear un sitio web con Drupal y elegir el tipo de enumeración
```
droopescan scan drupal -u <URL-TARGET> --enumerate <TYPE>
```

#### Tipos de enumeración
```
-p : plugin checks
-t : theme checks
-v : version checks
-i : interesting urls checks
```

#### Mostrar el estado de la herramienta
```
droopescan stats
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)