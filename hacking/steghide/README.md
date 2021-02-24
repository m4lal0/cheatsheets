# Steghide Cheat Sheet

#### Ocultar archivo en una imagen
```
steghide embed -ef <File> -cf <Image> -v
```

#### Extraer datos
```
steghide extract -sf <Image>
```

#### Extraer datos y sobreescribir si existe
```
steghide extract -sf <Image> -f
```

#### Ver información del archivo incrustado
```
steghide info <Image>
```

#### Comprimir el archivo antes de ocultarlo (El nivel puede ir de 1 al 9)
```
steghide embed -ef <File> -cf <Image> -z 2
```

#### No comprimir el archivo antes de ocultarlo
```
steghide embed -ef <File> -cf <Image> -Z
```

#### Ocultar archivo sin el nombre original del archivo
```
steghide embed -ef <File> -cf <Image> -N
```

#### Extraer archivo que no tiene nombre
```
steghide extract -sf <Image> -xf <NameFile>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)