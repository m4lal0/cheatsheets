# Evil-WinRM Cheat Sheet

#### Conexión usando usuario y contraseña
```
evil-winrm -i <IP-TARGET> -u '<USER>' -p '<PASSWORD>'
```

#### Conexión usando un NT Hash
```
evil-winrm -i <IP-TARGET> -u '<USER>' -H ':<NT-HASH>'
```

#### Conexión por SSL y proporcionando llave publica y privada
```
evil-winrm -i <IP-TARGET> -c <CERTIFICATE.pem> -k <PRIVATE-KEY.pem> -S
evil-winrm -i <IP-TARGET> -c <CERTIFICATE.pem> -k <PRIVATE-KEY.pem> -S -u '<USER>' -p '<PASSWORD>'
```

#### Descargar un archivo dentro de sesión evil-winrm
```
Evil-WinRM> download <FILE>
```

#### Cargar un archivo dentro de sesión evil-winrm
```
Evil-WinRM> upload <FILE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)