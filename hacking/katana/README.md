# Katana Cheat Sheet

#### Crawling a un sitio web
```
katana -u <URL>
```

#### Crawling a un sitio web y guardar el resultado
```
katana -u <URL> -o <OUTPUT>
```

#### Crawling y solo mostrar el path de los resultados
```
katana -u <URL> -fields path
```

#### Crawling y solo mostrar los archivos enconotrados
```
katana -u <URL> -fields file
```

#### Crawling y solo mostrar los directorios enconotrados
```
katana -u <URL> -fields dir
```

#### Crawling y solo mostrar los archivos que coincidan con las extensiones js,php,txt
```
katana -u <URL> -em js,php,txt
```

#### Crawling y nos mostrar los archivos que coincidan con las extensiones png,gif,woff
```
katana -u <URL> -ef png,gif,woff
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)