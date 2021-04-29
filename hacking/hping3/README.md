# Hping3 Cheat Sheet

### Enviar varios paquetes a un Host

#### *100,000 paquetes de Ping*
```
hping3 [IP-Address] -c 100000
```

### Exploración de puertos y descubrimiento de servicios

#### *Escaneo ACK a un puerto de un Host*
```
hping3 -A [IP-Address] -p [Port] -c [Package-Number]
```

#### *Escaneo SYN a los primeros 100 puertos de un Host*
```
hping3 -8 0-100 -S [IP-Address] -V
```

#### *Escaneo FIN, PUSH y URG a un puerto de un Host*
```
hping3 -F -P -U [IP-Address] -p [Port] -c [Package-Number]
```

#### *Escaneo ICMP a un puerto de un Host*
```
hping3 -1 [IP-Address] -p [Port] -c [Package-Number]
```

#### *Escaneo UDP a un puerto de un Host*
```
hping3 -2 [IP-Address] -p [Port] -c [Package-Number]
```

#### *Escaneo de subred completo para un Host*
```
hping3 -1 [Target-Subred] --rand-dest -I eth0
```

### Escanear más allá del Firewall/IDS

#### *Personalizar paquetes UDP*
```
hping3 [IP-Address] --udp --ran-source --data 500
```

#### *Inundación de TCP*
```
hping3 [IP-Address] --flood
```

### DoS Attack

#### *SYN Flooding*
```
hping3 -S [IP-Address] -a [Spoofable-IP-Address] -p 22 --flood
```

#### *PoD Attack*
```
hping3 -d 65538 -S -p 21 --flood [IP-Address]
```

#### *UDP Flood Attack*
```
hping3 -2 -p 139 --flood [IP-Address]
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)