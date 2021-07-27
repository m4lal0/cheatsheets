# SCP Cheat Sheet

#### Download File
```
scp user@IP-Address:/Path/to/file /Path/to/Save
```

#### Upload File
```
scp <File> user@IP-Address:/Path/to/file
```

#### Copiar directorio local al Host remoto
```
scp -r <Directory> user@IP-Address:/Path/to/remote-directory
```

### Copiar un archivo de un Host remoto a otro Host remoto
```
scp user@IP-Host1:/Path/to/file user@IP-Host2:/Path/to/Host2/remote-directory
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)