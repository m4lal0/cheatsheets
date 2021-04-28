# Google Dorks Cheat Sheet

### Filtros de búsqueda

| Filtro | Descripción                    | Ejemplo                    |
| ------------- | ------------------------------ | ------------------------------ |
| **allintext**      | Busca ocurrencias de todas las palabras clave dadas.       | `allintext:"keyword"`       |
| **intext**   | Busca las apariciones de palabras clave todas a la vez o una a la vez.     | `intext:"keyword"`       |
| **inurl**   | Busca una URL que coincida con una de las palabras clave.     | `inurl:"keyword"`       |
| **allinurl**   | Busca una URL que coincida con todas las palabras clave de la consulta.     | `allinurl:"keyword"`       |
| **intitle**   | Busca apariciones de palabras clave en el título en todas o una.    | `intitle:"keyword"`       |
| **allintitle**   | Busca apariciones de palabras clave en el título todas a la vez.     | `allintitle:"keyword"`       |
| **site**   | Busca específicamente ese sitio en particular y enumera todos los resultados de ese sitio.    | `site:"www.google.com"`       |
| **filetype**   | Busca un tipo de archivo particular mencionado en la consulta.    | `filetype:"pdf"`       |
| **link**   | Este operador busca sitios web o páginas que contienen enlaces al sitio web o página especificados.    | `link:"keyword"`       |
| **numrange**      | Se usa para ubicar números específicos en sus búsquedas.       | `numrange:321-325`       |
| **before/after**      | Se usa para buscar dentro de un rango de fechas en particular.       | `filetype:"pdf" & (before:2000-01-01 after:2001-01-01)`       |
| **inanchor**      | Esto muestra los sitios que tienen los términos clave en los enlaces que apuntan a ellos, en orden de mayor número de enlaces.       | `inanchor:rat`       |
| **allinanchor**      | La consulta solo devuelve páginas en las que el texto de anclaje de los enlaces a las páginas contiene las palabras "mejor", "nube", "servicio" y "proveedor" .       | `allinanchor: mejor proveedor servicio nube`       |
| **allinpostauthor**      | Exclusivo para la búsqueda de blogs, este selecciona publicaciones de blog escritas por personas específicas.       | `allinpostauthor:"keyword"`       |
| **related**      | Muestra las páginas web que son "similares" a una página web específica.       | `related:www.google.com`       |
| **cache**      | Muestra la versión de la página web que Google tiene en su caché.       | `cache:www.google.com`       |
| **info**      | Este operador busca información para la página web especificada.       | `info:keyword`       |
| **location**      | Este operador busca información para una ubicación específica.       | `location:keyword`       |
| **define**      | Busca definciones de palabras.       | `define:keyword`       |
| **weather**      | Nos mostrará el clima de la parte del mundo que queramos ver.       | `wather:keyword`       |
| **stock**      | Nos mostrará informacion financiera.       | `stock:keyword`       |
| **date**      | Busca solamente en un rango de meses (De la fecha actual hacia atrás).       | `date:3`       |
| **phonebook**      | Muestra listado de telefonos.       | `phonebook:keyword`       |

### Símbolos para usar en la búsqueda

| Filtro | Descripción                    | Ejemplo                    |
| ------------- | ------------------------------ | ------------------------------ |
| **" "**      | Comillas, buscar frase exacta.       | `"keyword"`       |
| **+**      | Incluir alguna palabra.       | `+keyword`       |
| **-**      | Excluir alguna palabra.       | `-keyword`       |
| *      | Asterisco, comodín, cualquier palabra, pero una sóla palabra.       | `*.google.com`       |

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)