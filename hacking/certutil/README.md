# Certutil Cheat Sheet

#### Encoding
```
certutil -encode file.txt encoded.txt
```

#### Decoding
```
certutil -decode encoded.txt decoded.txt
```

#### Hashing
```
certutil -hashfile ".\file.txt" md5
certutil -hashfile ".\file.txt" sha1
certutil -hashfile ".\file.txt" sha256
```

#### Downloading
```
certutil -f -urlcache -split http://7-zip.org/a/7z1604-x64.exe
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)