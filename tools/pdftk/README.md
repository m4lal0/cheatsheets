# PDFtk command Cheat Sheet

#### Unir dos PDF en uno solo
```
pdftk FILE-1.pdf FILE-2.pdf cat output FILE.pdf
```

#### Proteger con contraseña un PDF
```
pdftk FILE.pdf output FILE-NEW.pdf user_pw "PASSWORD"
```

#### Proteger con contraseña un PDF y para impresión también
```
pdftk FILE.pdf output FILE-NEW.pdf user_pw "PASSWORD" allow printing
```

#### Desencriptar un PDF
```
pdftk FILE.pdf input_pw "PASSWORD" output FILE-NEW.pdf
```

#### Reparar un PDF
```
pdftk FILE.pdf output FILE-NEW.pdf
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)