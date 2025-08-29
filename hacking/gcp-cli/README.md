# GCP CLI Cheat Sheet

#### Usar GCP local
```
gcloud auth application-default login
```

#### Usar una cuenta diferente
```
gcloud config set account <ACCOUNT>
```

#### Usar la cuenta por default
```
gcloud config set account default
```

#### Visualizar las configuraciones realizadas
```
gcloud info
```

#### Visualizar los proyectos a los que tenemos acceso y su ID correspondiente
```
gcloud projects list
```

#### Usar un proyecto proporcionando su ID
```
gcloud config set project <ID-PROJECT>
```

#### Saber la key de la cuenta de servicio
```
cat /root/.config/gcloud/application_default_credentials.json
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)