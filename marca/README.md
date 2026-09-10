# La marca

Dos canales que se juntan en un nodo. El logotipo no cambió de idea; cambió de
tronco, de color en claro, y ahora tiene las piezas que le faltaban.

## Qué usar

| Archivo | Dónde |
| --- | --- |
| `../profile/legiosdark.svg` | El lockup sobre fondo oscuro. |
| `../profile/legioslight.svg` | El lockup sobre fondo claro, teal plano. |
| `legios-mark.svg` | Sólo la marca, degradado, fondo oscuro. |
| `legios-mark-teal.svg` | Sólo la marca, un tono, fondo claro. |
| `legios-mark-mono.svg` | Un solo color, hereda del texto. Impresión y terminal. |
| `legios-favicon.svg` | 16 y 32 px. Trazo grueso, nodo grande. |
| `legios-mark-etch.svg` | Cuatro líneas de corte para el láser de la caja. |
| `icono/legios-icono-teal-blanco.png` | **El icono de la organización.** 1024², cuadrado. |
| `icono/legios-icono-como-hoy.png` | La alternativa, degradado sobre navy. |
| `colores/` | Los doce colorways probados, por si hace falta volver. |
| `legios-mark-3canales.svg` | La geometría vieja. Se guarda; no se usa. |

## Los dos cambios

**Tronco corto.** El trazo recto iba de `x9` a `x41`: a lo ancho de toda la
marca, o sea que era un tercer canal. Ahora arranca en `x34` y es el curso al
que los otros dos llegan. Dos canales, un curso. No se redibujó ninguna curva.

**Teal plano en claro.** Los dos SVG traían los mismos stops de degradado: la
versión clara sólo cambiaba el color de la palabra, así que la punta celeste
quedaba en **1.51:1 sobre blanco** y media marca no se veía. En claro va ahora
`#189AB0` plano — **3.34:1**, un archivo, sin degradado que mantener.

Sobre oscuro el degradado queda como estaba: `#5AE5F1 → #1E6EEF`.

## El icono de la organización

GitHub no acepta SVG para el avatar: van los PNG de `icono/`, cuadrados, 1024².
El avatar se recorta en círculo, por eso lleva la marca sola y no el lockup, con
margen de sobra para que el recorte no muerda nada.

## Una trampa

`currentColor` **no cruza un `<img src>`**. `legios-mark-mono.svg` referenciado
como imagen se dibuja negro. Va embebido en el HTML o el Markdown, o pisale el
`fill` desde afuera.

## La geometría

Caja de 64. Las mismas curvas en todas las variantes:

    M9 14 C26 14 28 32 41 32     canal de arriba
    M9 50 C26 50 28 32 41 32     canal de abajo
    M34 32 H41                   el tronco
    nodo: cx 50, cy 32, r 7.5

Trazo 5, puntas redondas, canales al 75% de opacidad y el nodo al 100%.
