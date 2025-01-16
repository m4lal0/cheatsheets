# AWS CLI Cheat Sheet

#### Configurar AWS consola
```
aws configure
```

#### Configurar AWS consola pero con otro perfil
```
aws configure --profile <NAME>
```

#### Obtener el ID de la cuenta que configuramos
```
aws sts get-caller-identity
```

#### Listar los usuarios de IAM
```
aws iam list-users
```

#### Ejecutar algun comando pero con otro perfile de IAM
```
aws iam list-users --profile <NAME>
```

#### Revisar los accesos al bucket
```
aws s3api get-bucket-acl --bucket <NAME-BUCKET>
```

#### Ver la información que tenga el bucket
```
aws s3 ls s3://<NAME-BUCKET>/ --recursive
```

#### Descargar un archivo a nuestro equipo
```
aws s3 cp s3://<NAME-BUCKET/<PATH-TO-FILE> <NAME-DIRECTORY_LOCAL-PATH>
```

#### Otra manera de descargar un archivo
```
aws s3api get-object --bucket <NAME-BUCKET> --key /upload/profile_avatar/secret.txt output.txt
```

#### Saber el Key y Access Key que configuramos en AWS CLI
```
cat /root/.aws/credentials
```

#### Saber las configuraciones que configuramos en AWS CLI
```
cat /root/.aws/config
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)