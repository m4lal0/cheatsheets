# exe2hex Cheat Sheet

#### Crear un archivo BATch y PowerShell a través de un EXE
```
exe2hex -x <EXE-FILE>
```

#### Crear un archivo BATch a través de un EXE
```
exe2hex -x <EXE-FILE> -b <OUTPUT.bat>
```

#### Crear un archivo PowerShell a través de un EXE
```
exe2hex -x <EXE-FILE> -p <OUTPUT.cmd>
```

#### Crear un archivo BATch y PowerShell a través del contenido de un ejecutable
```
echo <EXE-FILE> | exe2hex -s -b <OUTPUT.bat> -p <OUTPUT.cmd>
```

#### Crear un archivo BATch y PowerShell a través de un EXE y comprimirlo
```
exe2hex -x <EXE-FILE> -cc
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)