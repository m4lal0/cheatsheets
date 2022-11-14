# Hakrawler Cheat Sheet

#### Crawling a una URL
```
echo <URL> | hakrawler
```

#### Crawling a una URL y mostrar los resultado en JSON
```
echo <URL> | hakrawler -json
```

#### Crawling a múltiples URLs
```
cat urls.txt | hakrawler
```

#### Crawling a una URL y enviar las respuestas a un proxy
```
echo <URL> | hakrawler -proxy http://localhost:8080
```

#### Crawling a una URL incluyendo subdominios
```
echo <URL> | hakrawler -subs
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)