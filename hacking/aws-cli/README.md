# AWS CLI Cheat Sheet

#### Configurar AWS consola
```
aws configure
```

#### Configurar AWS consola pero con otro perfil
```
aws configure --profile <NAME>
```

#### Listar los perfiles configurados
```
aws configure list-profiles
```

#### Configurar el Access Key en un perfil
```
aws configure set aws_access_key_id <ACCESS-KEY> --profile <NAME>
```

#### Configurar el Secret Access en un perfil
```
aws configure set aws_secret_access_key <SECRET-KEY> --profile <NAME>
```

#### Configurar el Token Session en un perfil
```
aws configure set aws_session_token <TOKEN> --profile <NAME>
```

#### Obtener el ID y su ARN de la cuenta que configuramos (Servicio de Token de Seguridad (STS))
```
aws sts get-caller-identity --profile <NAME>
```

#### Mostrarnos la cuenta asociada a un Access Key
```
aws sts get-access-key-info --access-key-id=<ACCESS-KEY>
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