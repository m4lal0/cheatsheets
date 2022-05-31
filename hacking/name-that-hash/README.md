# Name-That-Hash command Cheat Sheet

#### Determinar el tipo de hash
```
nth -t "5f4dcc3b5aa765d61d8327deb882cf99"
```

#### Determinar el tipo de hash desde un archivo
```
nth -f <FILE-NAME>
```

#### Determinar el tipo de hash y que el resultado sea en formato JSON
```
nth -t "5f4dcc3b5aa765d61d8327deb882cf99" -g
```

#### Determinar el tipo de hash y no mostrar información de John the Ripper
```
nth -t "5f4dcc3b5aa765d61d8327deb882cf99" --no-john
```

#### Determinar el tipo de hash y no mostrar información de Hashcat
```
nth -t "5f4dcc3b5aa765d61d8327deb882cf99" --no-hashcat
```


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)