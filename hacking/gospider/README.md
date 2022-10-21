# GoSpider Cheat Sheet

#### Realizar un crawling a un sitio web y solo mostrar URLs
```
gospider -q -s "<URL>" 
```

#### Realizar un crawling a un sitio web, guardar el resultado
```
gospider -s ""<URL>"" -o <OUTPUT_FOLDER> -c 10 -d 1
```

#### Realizar un crawling a un listado de sitios
```
gospider -S <URLS_FILE> -o <OUTPUT_FOLDER> -c 10 -d 1 -t 20
```

#### Realizar un crawling y también obtener resultados de terceros (Archive.org, CommonCrawl.org, VirusTotal.com, AlienVault.com)
```
gospider -s "<URL>" -o <OUTPUT_FOLDER> -c 10 -d 1 --other-source
```

#### Realizar un crawling y también obtener resultados de terceros e incluir subdominios
```
gospider -s "<URL>" -o <OUTPUT_FOLDER> -c 10 -d 1 --other-source --include-subs
```

#### Realizar un crawling, obtener resultados de terceros y modificar la cabecera HTTP
```
gospider -s "<URL>" -o <OUTPUT_FOLDER> -c 10 -d 1 --other-source -H "Accept: */*" -H "Test: test" --cookie "testA=a; testB=b"
```

#### Realizar un crawling y excluir resultados como archivos con extensión woff o pdf
```
gospider -s "<URL>" -o <OUTPUT_FOLDER> -c 10 -d 1 --blacklist ".(woff|pdf)"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)