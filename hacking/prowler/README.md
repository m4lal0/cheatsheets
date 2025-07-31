# Prowler Cheat Sheet

## AWS - Amazon Web Services

#### Ejecutar la revisión de AWS usando un perfil de AWS CLI
```
prowler aws --profile IQSEC-PT
```

## GCP - Google Cloud Platform

#### Usar un archivo JSON de llave de authenticación de la cueta de servicio de Google
```
prowler gcp --credentials-file <PATH>
```

#### Ejecutar la revisión a un proyecto en especifico ó varios proyectos
```
prowler gcp --project-ids <ID-PROJECT>

prowler gcp --project-ids <ID-PROJECT-1> <ID-PROJECT-2> <ID-PROJECT-3> 
```

#### Mostrar una lista de servicios a los que tiene acceso nuestro usuario
```
prowler gcp --list-services
```

#### Mostrar una lista de las categorias a los que tiene acceso nuestro ausuario
```
prowler gcp --list-categories
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)