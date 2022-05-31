# Gobuster Cheat Sheat

## Modo: Fuzzing Sitio Web

#### Fuzzing a una URL y usando una wordlist especifica
```
gobuster dir --url <URL> -w <Wordlist>
```

#### Fuzzing a una URL, usando una wordlist especifica y guardar el resultado en un archivo
```
gobuster dir --url <URL> -w <Wordlist> -o <FileName>
```

#### Fuzzing a una URL y usando hilos para ir más rápido
```
gobuster dir --url <URL> -w <Wordlist> -t 100
```

#### Fuzzing a una URL y no mostrar el código 404 HTTP
```
gobuster dir --url <URL> -w <Wordlist> -b "404"
```

#### Fuzzing a una URL y mostrar los códigos 200 y 301 HTTP
```
gobuster dir --url <URL> -w <Wordlist> -s "200,301"
```

#### Fuzzing a una URL realizar redireccionamientos
```
gobuster dir --url <URL> -w <Wordlist> -r
```

#### Buscar por extensiones
```
gobuster dir --url <URL> -w <Wordlist> -x php,txt,js
```

#### Fuzzing a una URL y definir un User-Agent
```
gobuster dir --url <URL> -w <Wordlist> -a <AgentString>
```

## Modo: Enumerar Subdominios

#### Obtener subdominios o enumeración de virtual hosting
```
gobuster vhost -u <URL> -w <Wordlist> -t 200
```

## Modo: Subdominos DNS

#### Fuerza bruta para obtener subdominios DNS de un dominio
```
gobuster dns -d <Domain> -w <Wordlist>
```

#### Fuerza bruta para obtener subdominios DNS de un dominio y usando hilos para ir más rápido
```
gobuster dns -d <Domain> -w <Wordlist> -t 100
```

#### Obtener subdominios y mostrar la dirección IP de cada uno
```
gobuster dns -d <Domain> -w <Wordlist> -i
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)