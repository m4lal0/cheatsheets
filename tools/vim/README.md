# Vim Cheat Sheet

## Modo normal

### Navegación

+ `b` - ir a la palabra anterior
+ `w` - ir a la palabra siguiente
+ `e` - ir al final de la siguiente palabra
+ `j` - abajo
+ `h` - izquierda
+ `k` - arriba
+ `l` - derecha
+ `0` - ir al inicio de la linea
+ `$` - ir al final de la linea
+ `gg` - mover cursor al inicio del archivo
+ `G` - mover cursor al final del archivo
+ `#G` - para movernos a una linea en especifica del archivo (donde '#' es el número de línea, ej. 16G - Se mueve a la linea 16 del archivo)
+ `gd` - ir a la definición
+ `gf` - ir a la definición en el archivo
+ `ctrl + o` - regresar al archivo anterior despues de encontrar la definición
+ `ctrl + i` - volver al archivo para encontrar nuevamente la definición
+ `ctrl + g` - nos indica en que linea esta posicionado el cursor
+ `%` - salto al correspondiente parentesis, llaves ó corchetes, para encontrar cual es su inicio y fin de cada uno

### Inserción

+ `i` - insertar antes del cursor
+ `a` - insertar después del cursor
+ `A` - insertar al final de la línea

### Edición

+ `x` - suprimir
+ `yy` - copiar línea entera
+ `dw` - borrar palabra delante del cursor
+ `db` - borra palabra antes del cursor
+ `dd` - eliminar línea completa y no deja línea vacia
+ `d$` - eliminar desde el cursor sin eliminar la línea vacia
+ `p` - pegar en la línea de abajo
+ `P` - pegar en la línea de arriba
+ `u` - deshacer
+ `ctrl + r` - rehacer
+ `cw` - reemplazar palabra que esta delante del cursor
+ `ciw` - reemplazar palabra sin importar en que posicion este el cursor en la palabra
+ `r` - reemplazar un caracteres que esta delante del cursor
+ `R` - reemplazar todos los caracteres que esta delante del cursor
+ `o` - crea una linea nueva debajo del cursor
+ `O` - crea una linea nueva arriba del cursor

### Buscar

+ `/palabra` - para buscar una palabra, buscará en adelante de la posición del cursor
+ `?palabra` - para buscar una palabra, buscará atrás de la posición del cursor
+ `n` - siguiente coincidencia de la palabra encontrada
+ `N` - regresar a una coincidencia de la palabra encontrada

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

+ `v` - entrar a modo visual
+ `aw` - seleccionar palabra
+ `y` - copiar texto seleccionado
+ `d` - borrar texto seleccionado
+ `esc` - salir del modo visual
+ `>` - indentar a la derecha
+ `<` - indentar a la izquierda

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)