# Gobuster Cheat Sheat

## Modo: Fuzzing Sitio Web

#### Fuzzing a una URL y usando una wordlist especifica
```
gobuster dir --url <URL> -w <WORDLIST>
```

#### Fuzzing a una URL, usando una wordlist especifica y agregando un slash al final
```
gobuster dir --url <URL> -w <WORDLIST> --add-slash
```

#### Fuzzing a una URL, usando una wordlist especifica y guardar el resultado en un archivo
```
gobuster dir --url <URL> -w <WORDLIST> -o <FILE-NAME>
```

#### Fuzzing a una URL y usando hilos para ir más rápido
```
gobuster dir --url <URL> -w <WORDLIST> -t 100
```

#### Fuzzing a una URL y no mostrar el código 404 HTTP
```
gobuster dir --url <URL> -w <WORDLIST> -b 404
```

#### Fuzzing a una URL y mostrar los códigos 200 y 301 HTTP
```
gobuster dir --url <URL> -w <WORDLIST> -s 200,301
```

#### Fuzzing a una URL y no mostrar los resultados que contengan tamaño 0 y 404
```
gobuster dir --url <URL> -w <WORDLIST> --exclude-length 0,404
```

#### Fuzzing a una URL realizar redireccionamientos
```
gobuster dir --url <URL> -w <WORDLIST> -r
```

#### Buscar por extensiones
```
gobuster dir --url <URL> -w <WORDLIST> -x txt,php,sh,cgi,html,zip,bak,sql,old,js
```

#### Fuzzing a una URL y definir un User-Agent
```
gobuster dir --url <URL> -w <WORDLIST> -a <AGENT-STRING>
```

## Modo: Enumerar Subdominios

#### Obtener subdominios o enumeración de virtual hosting
```
gobuster vhost -u <URL> -w <WORDLIST> -t 200 --append-domain
```

## Modo: Subdominos DNS

#### Fuerza bruta para obtener subdominios DNS de un dominio
```
gobuster dns -d <DOMAIN> -w <WORDLIST>
```

#### Fuerza bruta para obtener subdominios DNS de un dominio y usando hilos para ir más rápido
```
gobuster dns -d <DOMAIN> -w <WORDLIST> -t 100
```

#### Obtener subdominios y mostrar la dirección IP de cada uno
```
gobuster dns -d <DOMAIN> -w <WORDLIST> -i
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)