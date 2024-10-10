# S3scanner Cheat Sheet

#### Buscar S3 buckets abiertos
```
s3scanner -bucket <BUCKET_NAME>
```

#### Buscar a traves de un listado de S3 buckets que esten abiertos
```
s3scanner -bucket-file <FILE_NAME>
```

#### Enumerar los buckets y proporcionando el provider (AWS)
```
s3scanner -bucket <BUCKET_NAME> -enumerate -provider aws
```

#### Buscar S3 buckets abiertos y dar mas información
```
s3scanner -bucket <BUCKET_NAME> -verbose
```

#### Enumerar los buckets, proporcionando el provider (AWS) y dando el resultado en json
```
s3scanner -bucket <BUCKET_NAME> -enumerate -provider aws -json
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)