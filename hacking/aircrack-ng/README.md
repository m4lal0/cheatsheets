# Aircrack-ng Cheat Sheet

#### Cracking password dando un nombre de BSSID
```
aircrack-ng -b <BSSID> <File.cap>
```

#### Cracking password dando un nombre de ESSID
```
aircrack-ng -e <ESSID> <File.cap>
```

#### Cracking password para WPA/WPA2 usando una Wordlist
```
aircrack-ng -w <Wordlist> <File.cap>
```

#### Cracking password para WEP dando un nombre de ESSID y almacenarlo en un archivo 
```
aircrack-ng -a 1 -e <ESSID> -l <Output-File> <File.cap>
```

#### Crear archivo Hashcat (HCCAP)
```
aircrack-ng -J <Name-Hascat> <File.cap>
```

#### Crear archivo Hashcat v3.6+ (HCCAP)
```
aircrack-ng -j <Name-Hascat> <File.cap>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)