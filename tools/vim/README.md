# Vim Cheat Sheet

## Modo normal

### Navegación

+ <kbd>b</kbd> - ir a la palabra anterior
+ <kbd>w</kbd> - ir a la palabra siguiente
+ <kbd>e</kbd> - ir al final de la siguiente palabra
+ <kbd>j</kbd> - abajo
+ <kbd>h</kbd> - izquierda
+ <kbd>k</kbd> - arriba
+ <kbd>l</kbd> - derecha
+ <kbd>0</kbd> - ir al inicio de la linea
+ <kbd>$</kbd> - ir al final de la linea
+ <kbd>gg</kbd> - mover cursor al inicio del archivo
+ <kbd>G</kbd> - mover cursor al final del archivo
+ <kbd>#G</kbd> - para movernos a una linea en especifica del archivo (donde '#' es el número de línea, ej. 16G - Se mueve a la linea 16 del archivo)
+ <kbd>gd</kbd> - ir a la definición
+ <kbd>gf</kbd> - ir a la definición en el archivo
+ <kbd>ctrl</kbd> + <kbd>o</kbd> - regresar al archivo anterior despues de encontrar la definición
+ <kbd>ctrl</kbd> + <kbd>i</kbd> - volver al archivo para encontrar nuevamente la definición
+ <kbd>ctrl</kbd> + <kbd>g</kbd> - nos indica en que linea esta posicionado el cursor
+ <kbd>%</kbd> - salto al correspondiente parentesis, llaves ó corchetes, para encontrar cual es su inicio y fin de cada uno

### Inserción

+ <kbd>i</kbd> - insertar antes del cursor
+ <kbd>a</kbd> - insertar después del cursor
+ <kbd>A</kbd> - insertar al final de la línea

### Edición

+ <kbd>x</kbd> - suprimir
+ <kbd>yy</kbd> - copiar línea entera
+ <kbd>dw</kbd> - borrar palabra delante del cursor
+ <kbd>db</kbd> - borra palabra antes del cursor
+ <kbd>dd</kbd> - eliminar línea completa y no deja línea vacia
+ <kbd>d$</kbd> - eliminar desde el cursor sin eliminar la línea vacia
+ <kbd>p</kbd> - pegar en la línea de abajo
+ <kbd>P</kbd> - pegar en la línea de arriba
+ <kbd>u</kbd> - deshacer
+ <kbd>ctrl</kbd> + <kbd>r</kbd> - rehacer
+ <kbd>cw</kbd> - reemplazar palabra que esta delante del cursor
+ <kbd>ciw</kbd> - reemplazar palabra sin importar en que posicion este el cursor en la palabra
+ <kbd>r</kbd> - reemplazar un caracteres que esta delante del cursor
+ <kbd>R</kbd> - reemplazar todos los caracteres que esta delante del cursor
+ <kbd>o</kbd> - crea una linea nueva debajo del cursor
+ <kbd>O</kbd> - crea una linea nueva arriba del cursor

### Buscar

+ `/palabra` - para buscar una palabra, buscará en adelante de la posición del cursor
+ `?palabra` - para buscar una palabra, buscará atrás de la posición del cursor
+ <kbd>n</kbd> - siguiente coincidencia de la palabra encontrada
+ <kbd>N</kbd> - regresar a una coincidencia de la palabra encontrada

### Comandos

+ `:w` - guardar
+ `:q` - salir
+ `:wq` - guardar y salir
+ `:q!` - salir forzosamente
+ `:s/palabra/sustituirpor` - reemplazar la palabra por la primera ocurrencia encontrada de la linea donde esta el cursor
+ `:s/palabra/sustituirpor/g` - reemplazar la palabra por todas las ocurrencias encontradas de la linea donde esta el cursor
+ `:%s/palabra/sustituirpor/gc` - reemplazar la palabra por todas las ocurrencias encontradas que estan en el archivo

## Modo visual

### Selección texto

+ <kbd>v</kbd> - entrar a modo visual
+ <kbd>aw</kbd> - seleccionar palabra
+ <kbd>y</kbd> - copiar texto seleccionado
+ <kbd>d</kbd> - borrar texto seleccionado
+ <kbd>esc</kbd> - salir del modo visual
+ <kbd>></kbd> - indentar a la derecha
+ <kbd><</kbd> - indentar a la izquierda

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)