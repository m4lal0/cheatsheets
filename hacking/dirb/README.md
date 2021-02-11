# Dirb Cheat Sheat

#### Fuzzing a una URL y con una wordlist por default
```
dirb <URL>
```

#### Fuzzing a una URL y usando una wordlist definida
```
dirb <URL> -w <Wordlist>
```

#### Fuzzing a una URL, usando una wordlist definida y guardar el resultado en un archivo
```
dirb <URL> -w <Wordlist> -o <FileName>
```

#### Fuzzing a una URL, usando una wordlist definida e ignorando la respuesta del código 404 HTTP
```
dirb <URL> -w <Wordlist> -N 404
```

#### Buscando por las extensiones PHP y txt
```
dirb <URL> -w <Wordlist> -X .php,.txt
```

#### Buscando desde un listado de extensiones
```
dirb <URL> -w <Wordlist> -x <ExtsFile>
```

#### Fuzzing a una URL y usar Recursividad en los directorios encontrados
```
dirb <URL> -w <Wordlist> -R
```

#### Fuzzing a una URL y especificando un User-Agent
```
dirb <URL> -w <Wordlist> -a <AgentString>
```

#### Fuzzing a una URL y usando Autenticación HTTP
```
dirb <URL> -w <Wordlist> -u <Username:Password>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)