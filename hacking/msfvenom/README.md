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

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)