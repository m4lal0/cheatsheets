# Sublist3r Cheat Sheet

#### Enumerar subdominios de un Dominio
```
sublist3r -d <Domain> -v
```

#### Enumerar subdominios que solo tengan los puertos abiertos 80 y 443
```
sublist3r -d <Domain> -p 80,443
```

#### Enumerar subdominios y habilitar el modulo BruteForce
```
sublist3r -d <Domain> -b
```

#### Enumerar subdominios y utilizar motores específicos como Google, Yahoo y Virustotal
```
sublist3r -d <Domain> -e google,yahoo,virtustotal
```

#### Guardar los resultados en un archivo
```
sublist3r -d <Domain> -o <Output>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)