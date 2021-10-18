# Cisco IOS Cheat Sheet

### Comandos Básicos

+ Ver la ayuda
```
?
```
+ Entrar al equipo
```
enable
```
+ Entrar a la configuración del equipo
```
configure terminal
```
+ Guardar los cambios realizados lo que esta en RAM para guardarlo en NVRAM
```
# copy running-config startup-config
```
+ Colocarle nombre al equipo
```
# hostname <Name>
```
+ Reiniciar el equipo
```
# reload
```
+ Borrar el SO en la flash
```
# delete flash
```

### Comandos de verificación

+ Mostrar la configuración del router
```
# show run
```
+ Mostrar la versión del equipo
```
# show version
```
+ Mostrar la flash
```
# show flash
```
+ Mostrar configuraciones de VLANS
```
# show vlan
```
+ Mostrar la configuracion que esta en la memoria RAM
```
# show running-config
```
+ Mostrar el archivo de configuración inicial de NVRAM
```
# show startup-config
```
+ Mostrar informacion de que equipos tiene conectados directamente el router (solo funciona con equipos cisco)
```
# show cdp neighbors
# show cdp neighbors detail
```
+ Mostrar informacion detallada del CDP del equipo
```
# show cdp entry *
```
+ Ver en que interfaces esta habilitado el CDP
```
# show cdp interface
```
+ Ver si esta habilitado el CDP en el equipo
```
# show cdp
```
+ Mostrar las MAC de los equipos conectados al router
```
# show mac-address-table
```
+ Mostrar el Spanning-Tree
```
# show spanning-tree
```

### Configurar Password

+ Configurar un Password para Enable para el equipo
```
# enable password <password>
```
+ Configurar un Password para Telnet para el equipo
```
# line vty 0 4
# password <password>
# login
```
+ Configurar un Password para Consola para el equipo
```
# line console 0
# password <password>
# login
```
+ Configurar un Password para Enable Secret para el equipo (Para encriptar el password de Enable)
```
# enable secret <password>
```

### Recuperación de contraseña en router

- Debemos tener acceso fisico al equipo
- Reiniciamos el router y cuando este cargando dentro de CLI, presionamos Ctrl + Pause
para entrar en modo rommon
- Dentro de rommon ejecutamos lo siguiente:
```
rommon> confreg 0x2142
rommon> reset
```
- Con esto cuando reinicie el router, no encuentra la configuracion, pero ahi esta, solo cambiaremos la ubicación para que la tome:
```
router# show startup-config
router# copy startup-config running-config
router# configure terminal
```
- si el password está encriptado, lo modificamos o agregamos un nuevo password. Si no esta encriptado solo lo vemos con show startup-config:
```
router(config)# config-register 0x2102
router(config)# exit
router# copy running-config startup-config
router# reload
```

### Configuración de SSH

- Crear un usuario y una contraseña local
```
router(config)# username <user> privilege 15 password <password>
```
- Crear un dominio de host en el switch
```
router(config)# ip domain-name <domain>
```
- Activa el servidor SSH para la autenticacion local y remota, ademas genera una clave RSA
```
router(config)# crypto key generate rsa
```
- Configura el switch para que corra SSH version 2
```
router(config)# ip ssh version 2
```
- Ingresa a la configuracion VTY
```
router(config)# line vty 0 15
```
- Configura el protocolo de comunicacion SSH
```
router(config-line)# transport input ssh
```
- Autentica la interface VTY con las credenciales locales
```
router(config-line)# login local
```
- Despliega el servidor SSH esta activo y la version e información de configuracion
```
router# show ip ssh
```
- Muestra el estado del servidor SSH
```
router# show ssh
```

### Configuración básica de IPv6

- Habilitar el IPv6
```
router(config)# ipv6 unicast-routing
```
- Configurar el IPv6 en la interface
```
router(config)# interface serial 0/0/0
router(config-if)# ipv6 address 2001:0DB8:1c18:1111::3/64
router(config-if)# no shutdown
```
- Verificar el estado de la interfaz con IPv6 configurado
```
router# show ipv6 interface
router# show ipv6 interface brief
router# ping ipv6 2001:0DB8:1c18:1111::3
```

### Rutas estaticas con IPv6

- Configurar el IPv6 en la interface
```
router(config)# interface Giga 0/0
router(config-if)# ipv6 address FC00:111:111:111:111::1/64
router(config-if)# no shutdown
```
- Configurar la ruta con la IPv6 de la interface del otro lado, y con la IPv6 del otro router
```
router(config)# ipv6 route FC00:222:222:222::2/64 2001:10:10:10:2
```

## Switches

### Configuraciones básicas
+ Configurar una interface Ethernet
```
switch(config)# interface FastEthernet 0/0
```
+ Configurar una interface GigabitEthernet
```
switch(config)# interface GigabitEthernet 0/0
```
+ Configurar un rango de interface Ethernet
```
switch(config)# interface range FastEthernet 0/1 - 3
```
+ Configurar una Dirección IP en una interface
```
switch(config)# interface FastEthernet 0/0
switch(config-if)# ip address <IP> <Mascara>
switch(config-if)# no shutdown
```
+ Eliminar configuración del equipo
```
switch# erase startup-config
```

### Configuracion de IP administrativa
```
switch(config)# interface vlan 1
switch(config-if)# ip address 10.1.1.30 255.255.255.0
switch(config-if)# no shutdown
```

### VLANS

+ Crear una VLAN
```
switch(config)# vlan 10
switch(config-vlan)# name ventas
switch(config-vlan)# end
```
+ Asignar un puerto a una VLAN
```
switch(config)# interface fastEthernet 0/1
switch(config-if)# switchport mode access
switch(config-if)# switchport access vlan 10
```
+ Mostrar las VLANS
```
switch# show vlan
```
+ Mostrar la informacion de ese nombre de VLAN
```
switch# show vlan name ventas
```
+ Muestra informacion de ese ID de VLAN
```
switch# show vlan 10
```
+ Borrar las configuraciones de la VLANs
```
switch# delete vlan.dat
```

### TRUNKING

+ Configurar el switch en uno de sus puertos en modo trunk
```
switch(config)# interface fastEthernet 0/24
switch(config-if)# switchport mode trunk
```
+ Mostrar la informacion sobre Trunk
```
# show interfaces trunk
```

### VTP - VLAN TRUNKING PROTOCOL

+ Crear un Dominio
```
switch(config)# vtp domain malalo
```
+ Colocar un switch como Server
```
switch(config)# vtp mode server
```
+ Colocar un switch modo Cliente
```
switch(config)# vtp mode client
```
+ Colocar un switch en modo Transparente
```
switch(config)# vtp mode transparent
```
+ Mostrar informacion de VTP
```
# show vtp status
```
+ Habilitar VTP Prunning en el dominio
```
# vtp pruning
```

### InterVLAN ROUTING: ROUTER ON A STICK

+ Colocar la interfaz hacie el router en modo trunk
```
Switch(config)# interface fastEthernet 0/24
Switch(config)# switchport mode trunk
```
+ Activar la interfaz en el router
```
Router(config)# interface gigaethernet 0/0
Router(config-subif)# no shutdown
```
+ Crear la primera Subinterface y activar el protocolo 802.1q con la VLAN que corresponde (VLAN 100)
```
Router(config)# interface gigaethernet 0/0.100
Router(config-subif)# encapsulation dot1q 100
Router(config-subif)# ip address 10.1.1.254 255.255.255.0
```
+ Crear la segunda Subinterface y activar el protocolo 802.1q con la VLAN que corresponde (VLAN 200)
```
Router(config)# interface gigaethernet 0/0.200
Router(config-subif)# encapsulation dot1q 200
Router(config-subif)# ip address 10.2.1.254 255.255.255.0 
```
+ Comando de verificacion
```
# show running-config
# show ip interfaces brief
```

### SVI (Switch Virtual Interface) - Para Switches con Capa 3

+ Configurar una VLAN ya creada previamente y configurar su puerta de enlace
```
switch(config)# interface vlan 100
switch(config-if)# ip address 10.1.1.254 255.255.255.0
```
+ Comandos de verificacion
```
# show running-config
# show ip interfaces brief
```
+ Habilitar la tabla de enrutamiento
```
switch(config)#ip routing
```
+ Mostrar la tabla de enrutamiento
```
# show ip route
```

### SWITCHPORT ANALIZER (SPAN)

+ Configurar puerto FastEthernet0/1 como Puerto SOURCE
```
switch(config)# monitor session 1 source interface fastethernet 0/1
```
+ Configurar puerto FastEthernet0/2 como Puerto DESTINO
```
switch(config)# monitor session 1 destination interface fastethernet 0/2
```
+ Verificar la configuracion de SPAN
```
# show monitor session 1
```

### STACKWISE

+ Verificar la configuración
```
# show switch stack-ports
# show switch neighbors
# show switch
```

### ETHERCHANNEL - Agrupacion de interfaces fisicas en una sola interfaz logica

+ Crear una interfaz tipo Port-Channel y se asigna un numero y descripcion
```
switch(config)# interface port-channel 1
switch(config-if)# description Hacia SW2
```
+ Luego configurar en modo trunk para transmitir más de una VLAN
```
switch(config-if)# switchport mode trunk
```
+ Configurar las interfaces que estaran con Port-Channel
```
switch(config)# interface range fastEthernet 0/23 -24
switch(config-if-range)# switchport mode trunk
switch(config-if-range)# channel-group 1 mode desirable
```
+ Verificar configuración
```
# show running-config
# show interface port-channel 1
# show port-channel summary
# show etherchannel summary
```

## Routers

### ENRUTAMIENTO

+ Configurar una IP a la interfaz
```
router(config)# interface gigabitEthernet 0/0
router(config-if)# ip address 192.168.1.254 255.255.255.0
router(config-if)# no shutdown
```
+ Configurar la IP a la interfaz que tiene conectado a otro router
```
router(config)# interface gigabitEthernet 0/0
router(config-if)# ip address 10.1.1.1 255.255.255.252
router(config-if)# no shutdown
```

### ENRUTAMIENTO ESTATICO

+ Se configura la red donde se quiere llegar y la IP del siguiente salto (Es el que debe ser usado)
```
router(config)# ip route <RedDestino> <MascaraDestino> <NextHop>
router(config)# ip route 172.16.1.0 255.255.255.0 10.1.1.2
```
+ Se configura la red donde se quiere llegar y la interfaz de salida
```
router(config)# ip route <RedDestino> <MascaraDestino> <InterfazSalida>
```
+ Comandos de Verificacion
```
# show ip route
# show ip route static
# show running-config | include ip route
```

### EIGRP

+ Habilitar el protocolo de enrutamiento, seguido de un Sistema Autonomo que debe ser el mismo para los demas routers, Puede ir de 1 hasta 65535
```
router(config)# router eigrp <autonomous-system>
```
Ejemplo:
```
router(config)# router eigrp 100
```

+ Se configuran las direcciones de las redes DIRECTAMENTE conectadas que seran anunciadas por EIGRP
```
router(config-router)# network <Direccion-IP> <WildCard>
```
Ejemplo:
```
router(config-router)# network 192.168.1.0 0.0.0.255
router(config-router)# network 10.1.1.0 0.0.0.3
```

+ Evita que se resuman las rutas (sumarizacion) de redes discontinuas
```
router(config-router)# no auto-summary
```

+ En la INTERFAZ se debe configurar el ancho de banda real
```
router(config-if# bandwidth
```
+ Evita que una interfaz envie publicaciones
```
router(config-router)# passive-interface <tipo> <numero>
```
+ Comandos de verificacion
```
# show ip route : Muestra la tabla de enrutamiento
# show ip protocols : Muestra los parametros del protocolo
# show ip eigrp neighbors : Muestra la informacion de vecinos de EIGRP
# show ip eigrp topology : Muestra la tabla de topologia
# debug ip eigrp : Muestra en tiempo real la informacion de los paquetes de EIGRP
```

### OSPF

+ Habilitar el protocolo de enrutamiento, el numero debe ser diferente en cada router, para identificar
```
router(config)# router ospf <autonomous-system>
```
Ejemplo:
```
router(config)# router ospf 1
```
+ Se configuran las direcciones de las redes DIRECTAMENTE conectadas que seran anunciadas por OSPF
```
router(config-router)# network <Direccion-IP> <WildCard> area <ID-area>
```
Ejemplo:
```
router(config-router)# network 10.1.1.0 0.0.0.255 area 0
router(config-router)# network 172.16.1.0 0.0.0.3 area 0
router(config-router)# network 172.16.1.4 0.0.0.3 area 0
```
+ Comandos de verificacion
```
# show ip route : Muestra la tabla de enrutamiento
# show ip protocols : Muestra los parametros del protocolo
# show ip ospf neighbors : Muestra la informacion de vecinos de OSPF
```
+ Eliminar toda la configuracion de OSPF
```
router(config)# no router ospf 1
```

### OSPF - Router ID

+ Modificar el Router ID
```
router(config)# router ospf 1
router(config-router)# router-id 1.1.1.1
# clear ip ospf process
```

+ Quitar el Router ID
```
router(config)# router ospf 1
router(config-router)# no router-id 1.1.1.1
# clear ip ospf process
```
+ Si no funciona, se tiene que eliminar la configuracion completa del OSPF
```
router(config)# no router ospf 1
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)