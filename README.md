# elconfin.es

Web de **El Confín**, un sello editorial de libros de aventuras para lectores a partir de los
diez años. HTML estático servido con GitHub Pages. Sin build, sin dependencias, sin JavaScript
más allá del formulario.

## Estructura

```
├── index.html          la página
├── privacidad.html
├── aviso-legal.html
├── _pliego.css         estilos de la página
├── _legal.css          estilos de las dos páginas legales
├── .nojekyll           ← NO BORRAR (ver abajo)
├── CNAME               elconfin.es
├── robots.txt
└── assets/             imágenes, iconos y tipografías
```

### `.nojekyll` no se borra

GitHub Pages pasa los sitios por Jekyll, que **se salta los ficheros que empiezan por `_`**. Sin
ese fichero vacío, `_pliego.css` y `_legal.css` no llegarían a publicarse y la web saldría sin
estilos. Es la clase de fallo que cuesta media tarde encontrar.

## Cosas que conviene saber

**Las tipografías van autoalojadas** en `assets/fuentes-pliego.css`, incrustadas como data URI.
No se cargan de Google Fonts a propósito: en la UE, servir fuentes desde un tercero mete la IP
del visitante donde no hace falta.

**No hay cookies y no hay banner de cookies.** Es consecuencia de lo anterior y de no usar
analítica con cookies.

**Un solo mundo visual, sin modo oscuro.** El fondo de pergamino es parte de la identidad de la
casa y no se oscurece; todos los colores se declaran de forma explícita para que la página no
herede el tema de quien la abra.

## Estado actual

🚧 **En construcción.** La web está cerrada a buscadores —`robots.txt` con `Disallow: /` y
`noindex` en la página— mientras se termina de montar. Las tres cosas que faltan van marcadas
en el código con un comentario en mayúsculas que dice qué quitar y cuándo:

1. El aviso de maqueta del pie.
2. El recuadro punteado sobre la cubierta, que marca dónde irá el rótulo de la serie.
3. El envío del formulario, que todavía no está conectado a ningún gestor de correo.

Al quitarlas hay que borrar también los `noindex` y dejar el `robots.txt` en su versión
definitiva, que ya está escrita ahí dentro, comentada.

---

© Gervasio Varela Fernández. Los textos y las ilustraciones son míos. Las leyendas que se
cuentan son patrimonio popular y no son de nadie; lo mío es la manera de contarlas.
