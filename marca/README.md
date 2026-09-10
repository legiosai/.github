# La marca

El logotipo no cambia. Acá están las piezas que faltaban y el arreglo de una
que estaba mal.

## Qué usar

| Archivo | Dónde |
| --- | --- |
| `../profile/legiosdark.svg` | El lockup sobre fondo oscuro. Sin cambios. |
| `../profile/legioslight.svg` | El lockup sobre fondo claro. **Corregido**, ver abajo. |
| `legios-mark.svg` | Sólo la marca, para avatares y redes, sobre fondo oscuro. |
| `legios-mark-light.svg` | Sólo la marca, sobre fondo claro. |
| `legios-mark-mono.svg` | Un solo color, hereda del texto. Impresión y terminal. |
| `legios-favicon.svg` | 16 y 32 px. Trazo más grueso y nodo más grande. |
| `legios-mark-etch.svg` | Cuatro líneas de corte para el láser de la caja. |

## Lo que estaba mal

`legiosdark.svg` y `legioslight.svg` traían **los mismos stops de degradado**.
La versión clara sólo cambiaba el color de la palabra, no el de la marca, así
que la punta celeste quedaba en **1.51:1 sobre blanco** — media marca no se veía.

El stop claro pasa a `#189AB0`, que da **3.34:1** y sigue siendo el mismo cian.
Es el único cambio: la tipografía ya venía en curvas y no se tocó.

Sobre el fondo oscuro la marca ya daba 13.25:1 y quedó igual.

## Una trampa

`currentColor` **no cruza un `<img src>`**. `legios-mark-mono.svg` referenciado
como imagen se dibuja negro. Va embebido en el HTML o el Markdown, o pisale el
`fill` desde afuera.

## La geometría

Tres ramas que convergen en un nodo, en una caja de 64. Las mismas curvas del
lockup, por si hace falta redibujarlas:

    M9 32 H41
    M9 14 C26 14 28 32 41 32
    M9 50 C26 50 28 32 41 32
    nodo: cx 50, cy 32, r 7.5
