# Naabu Cheat Sheet

#### Escanear un objetivo
```
naabu -host <Target>
```

#### Escanear los objetivos dentro de un archivo
```
naabu -iL <File>
```

#### Escanear puertos especificos
```
naabu -p 80,443,21-23 -host <Target>
```

#### Escanear todos los puertos
```
naabu -p - -host <Target>
```

#### Excluir puertos en el análisis
```
naabu -p - -exclude-ports 80,443 -host <Target>
```

#### Mostrar solo los puertos encontrados en el objetivo
```
naabu -silent -host <Target>
```

#### Guardar los resultados en un archivo
```
naabu -host <Target> -o <Output>
```

#### Obtener los resultados en formato JSON
```
naabu -host <Target> -json
```

#### Validación de segunda capa de los puertos encontrados
```
naabu -host <Host> -verify
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)