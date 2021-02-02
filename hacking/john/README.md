# John the Ripper Cheat Sheet

#### Mostrar los tipos de contraseñas que John puede decifrar con la velocidad del crack (crack/segundo)
```
john --test
```

## Modos de Cracking

#### Para usar una lista de palabras
```
john --worlist=<Wordlist> <PasswordFile>
```

#### Modo incremental (Brute Force)
```
john --incremental <hashfile>
```

#### Usar una wordlist y una regla
```
john --worlist=<Wordlist> <PasswordFile> --rules=<RulesName>
```

#### Mostrar el listado de formatos que se pueden usar
```
john --list=formats
```

#### Forzar hash a un tipo de formato (Ejemplo formato NT)
```
john --format=NT <hashfile>
```

#### Mostrar resultados después de ejecutar John
```
john --show <hashfile>
```

## Sesión y Restauración

#### Restaurar una sesión de John interrumpida
```
john --restore:<name>
```

## Reglas

#### Tipos de reglas ya definidas
```
john --rules=Single
john --rules=Wordlist
john --rules=Extra
john --rules=Jumbo
john --rules=KoreLogic
john --rules=All
```

#### Crear una regla
```
[List.Rules:Tryout]
l
u
c
l r
l Az"2015"
d
l A0"2015"
A0"#"Az"#"
```

| Regla | Descripcion |
| :--------: | :-------- |
| l     | Convertir a minusculas     |
| u     | Convertir a mayusculas     |
| c     | Primera letra en mayusculas     |
| r     | Palabra al reves     |
| d     | Duplicar     |

###### Nota: Editar archivo john.conf

---
:::info
[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)
:::