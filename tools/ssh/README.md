# SSH Cheat Sheet

#### Conexión
```
ssh <USERNAME>@<HOST>
```

#### Conexión a puerto diferente
```
ssh <USERNAME>@<HOST> -p <PORT>
```

#### Conexión por medio de una clave privada
```
ssh -i <KEY-FILE> <USERNAME>@<HOST>
```

#### Conexión por un túner dinámico
```
ssh -D <PORT> <USERNAME>@<HOST>
```

#### SSH forwarding local
```
ssh <USERNAME>@<HOST> -N -f -L <LOCAL-PORT>:<TARGET-HOST>:<TARGET-PORT>
```

#### SSH ocultando nuestra conexión
```
ssh -o UserKnownHostsFile=/dev/null -T <USERNAME>@<HOST> 'bash -i'

Su usuario
- no se añade a /var/log/utmp
- no aparece en w o who cmd
- no tiene .profile o .bash_profile
```

### Configuraciones

#### Deshabilitar password para el SSH
```
sed -i 's/PasswordAuthentication yes/PasswordAuthentication no/g' /etc/ssh/sshd_config
```

#### Deshabilitar usuario root para el SSH
```
sed -i 's/^PermitRootLogin yes/#PermitRootLogin yes/' /etc/ssh/sshd_config
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)