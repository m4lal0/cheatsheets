# The Harvester Cheat Sheet

#### Identificar Emails de un dominio a traves de Google y Bing
```
theHarvester -d <Domain> -b google,bing
```

#### Limitar a 100 búsquedas
```
theHarvester -d <Domain> -b google -l 100
```

#### Buscar personas en Linkedin del dominio objetivo
```
theHarvester -d <Domain> -b linkedin
```

#### Obtener toda la información del sitio web victima
```
theHarvester -d <Domain> -b all
```

#### Guardar el resultado en un archivo HTML ó XML
```
theHarvester -d <Domain> -b all -f <FileName.html|FileName.xml>
```

#### Buscar en Shodan
```
theHarvester -d <Domain> -s
```

#### Ataque de Fuerza Bruta DNS
```
theHarvester -d <Domain> -c -b google
```

---
:::info
[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)
:::