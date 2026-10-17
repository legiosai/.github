<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="legiosdark.svg">
  <source media="(prefers-color-scheme: light)" srcset="legioslight.svg">
  <img alt="Legios" src="legioslight.svg" width="440">
</picture>

### Todo empieza siendo algo que necesitábamos nosotros

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="fichadark.svg">
  <source media="(prefers-color-scheme: light)" srcset="fichalight.svg">
  <img alt="19 repos · 6 públicos · 22 lenguajes · 2 personas" src="fichalight.svg" width="560">
</picture>

</div>

Somos dos personas. Cada repositorio que hay acá existe porque algo nos estaba
haciendo perder tiempo y en algún momento nos cansamos y lo arreglamos. Algunas
de esas cosas quedaron lo bastante bien como para que las use cualquiera, y ésas
son públicas. El resto se queda adentro, no porque sea secreto sino porque
todavía no anda solo.

Con el tiempo nos dimos cuenta de que casi todo lo que nos costaba era lo mismo
dicho de distintas maneras: había información que ya estaba en el disco y nadie
la miraba. Cuánta cuota quedaba. Qué comandos tiene este repo. De qué causa
salieron estos cuarenta incidentes. Las herramientas de acá son eso, mirar lo
que ya estaba ahí antes de llamar a un modelo o de pedirle a una persona que se
acuerde.

## Lo que podés usar hoy

<table>
<tr>
<td width="120" align="center" valign="middle">
  <img src="https://quartermaster.legios.com.ar/img/logo-256.png" width="88" alt="">
</td>
<td valign="middle">

### [quartermaster](https://github.com/legiosai/quartermaster)

Cuánta cuota te queda en **todos** los perfiles de Claude Code de la máquina,
más Codex y los proveedores que guarda opencode.
**Público y MIT.** · [Sitio](https://quartermaster.legios.com.ar/) ·
[Releases](https://github.com/legiosai/quartermaster/releases)

</td>
</tr>
</table>

Salió un día que nos quedamos sin cuota en la mitad de algo. La barra de arriba
decía 8 %. Cuando fuimos a ver, el cache de Claude Code tenía otra barra, sin
nombre, al 75 % y con aviso del servidor. Ninguna herramienta la mostraba porque
todas leen las dos que tienen nombre. Ésta lee todas, de todos los perfiles que
haya en la máquina, y no usa red ni credenciales: el número sale del cache que
Claude Code ya dejó en el disco, así que hay número aunque el token esté
vencido.

```bash
brew install legiosai/tap/quartermaster    # macOS
sudo apt install quartermaster             # Linux, con el repo de Legios agregado
scoop bucket add legios https://github.com/legiosai/scoop-bucket
scoop install quartermaster                # Windows
npm install -g @legios/quartermaster       # cualquier sistema con Node
```

<p align="center">
  <img src="https://quartermaster.legios.com.ar/img/barra.png" width="520" alt="La barra de arriba de GNOME con un medidor por cuenta">
</p>

La fórmula de Homebrew vive en
[`homebrew-tap`](https://github.com/legiosai/homebrew-tap) porque Homebrew exige
que un tap se llame así y sea público, y el manifiesto de Windows en
[`scoop-bucket`](https://github.com/legiosai/scoop-bucket) por la misma razón.
Son unas líneas y una suma de verificación cada uno; no hay nada más ahí.

<table>
<tr>
<td width="120" align="center" valign="middle">
  <img src="https://archivist.legios.com.ar/favicon.svg" width="88" alt="">
</td>
<td valign="middle">

### [archivist](https://github.com/legiosai/archivist)

Todo lo que tenés para leer o mirar —manga, cómics, películas, series y anime— servido desde
tu propio disco, con un solo estante de «seguir» para todo y una API para tus herramientas.
**Público y MIT.** · [Sitio](https://archivist.legios.com.ar/) ·
[Changelog](https://github.com/legiosai/archivist/blob/main/CHANGELOG.md)

</td>
</tr>
</table>

Un lector y un reproductor en uno, auto-alojado, para lo que ya está en carpetas: recuerda el
tomo, la página, el episodio y el minuto, y la misma historia en manga y en anime es una sola
obra con un solo lugar donde seguir. Hay un perfil para cada persona de la casa, OPDS para
leer desde el celular y un servidor MCP para agentes. Nunca trae obras: ni descargas, ni
scraping, ni listas de fuentes; lee lo que ponés en sus carpetas.
*0.7, al 2026-10-06.*

```bash
docker build -t archivist https://github.com/legiosai/archivist.git
docker run -d -p 8780:8780 -v /ruta/a/la/biblioteca:/library -v archivist-data:/data \
  -e ARCHIVIST_TOKEN="$(openssl rand -hex 24)" archivist
```

<p align="center">
  <img src="https://archivist.legios.com.ar/img/library.jpg" width="520" alt="La biblioteca de archivist: el estante de seguir y todas las obras">
</p>

<table>
<tr>
<td width="120" align="center" valign="middle">
  <img src="https://tidbit.legios.com.ar/favicon.svg" width="88" alt="">
</td>
<td valign="middle">

### [tidbit](https://github.com/legiosai/tidbit)

El diccionario tech, explicado fácil: qué es una API, un token, un data lake o una VPN, en
palabras simples y en castellano y en inglés.
**Público y MIT.** · [Sitio](https://tidbit.legios.com.ar/es/) ·
[Para desarrolladores](https://tidbit.legios.com.ar/es/developers/)

</td>
</tr>
</table>

Es para gente curiosa que no es ingeniera, que escucha GPU, S3 o Kubernetes y quiere
entenderlo en cinco minutos. Cada término tiene una definición de una línea, una analogía de
todos los días, un diagrama y los links a la documentación oficial, y enlaza a los otros
términos que usa, así que se puede seguir el hilo desde lo básico. Cada día que entrás te
muestra uno que todavía no viste. También se lee con código: Markdown en cualquier página, una
API JSON y un servidor MCP en `/mcp`, sin cuenta.
*102 términos en 9 temas, al 2026-10-17.*

<p align="center">
  <a href="https://tidbit.legios.com.ar/es/"><img src="https://tidbit.legios.com.ar/og-es.png" width="520" alt="Tidbit: el diccionario tech, explicado fácil"></a>
</p>

<table>
<tr>
<td width="120" align="center" valign="middle">
  <img src="https://sunandmoon.legios.com.ar/brand/logo-256.png" width="88" alt="">
</td>
<td valign="middle">

### [Sun and Moon](https://sunandmoon.legios.com.ar)

Un juego de plataformas y puzzles para dos, en el navegador: el Sol y la Luna se cruzan una
hora por eclipse y sólo pasan las salas si se apoyan uno en el otro.
**Gratis para jugar; el código es privado.** · [Jugar](https://sunandmoon.legios.com.ar) ·
Un juego de Legios y Sol Soletti

</td>
</tr>
</table>

El Sol camina por el fuego solar y la Luna por la luz de luna; cada uno muere en el elemento
del otro, y una sala se abre sólo cuando cada uno está en su puerta. Se juega con un solo
teclado o en línea entre dos navegadores, en castellano y en inglés.

<p align="center">
  <img src="https://sunandmoon.legios.com.ar/og.png" width="520" alt="El menú de Sun and Moon: el eclipse sobre el balcón del castillo, entre una torre dorada y una plateada">
</p>

## Lo que se queda adentro

Todo lo de esta sección es privado. Está descrito y no enlazado para no mandarte
a un 404, y cada estado lleva su fecha porque un estado sin fecha envejece
mintiendo.

**`cartographer`** · Un agente en un repo nuevo gasta la mayor parte de
sus llamadas en `ls`, `grep` y leer configs para enterarse de cosas que el repo
ya sabe de sí mismo. El cartógrafo calcula eso una vez —stack, comandos, entry
points, símbolos, referencias— sin modelo y sin red, y lo deja en un mapa que
se consulta. Lo que no puede saber lo deja en `null`, no lo adivina.
*Vía C, C0 a C9 hechos. Al 2026-09-10.*

**`healer`** · Nadie quería seguir persiguiendo tracebacks a mano.
Toma incidentes reales, los agrupa por causa en vez de por evento, arma un
legajo con citas al código y recién ahí llama al modelo, una vez por grupo. Del
otro lado sale una spec, nunca un merge: es lo único de acá que se dispara solo
sin una persona adelante, y por eso no toca `main`.
*Vía H, H0 a H3 y H5 a H7 mergeados. Veintisiete hipótesis esperan revisión
humana; la tasa de aceptación todavía es `null`. Al 2026-09-10.*

**`pipeline`** · En la versión anterior teníamos veintiséis agentes. La
mayoría eran funciones con nombre de persona: uno abría PRs, otro leía issues,
otro miraba checks. Ahora hay un solo ejecutor, externo, que recibe una spec y
devuelve un PR, y el aislamiento donde corre se probó en verde y en rojo.
*Fase C, P0 a P6 cerrados, P7 abierto. El north star —PRs mergeados sin que
un humano reescriba el cambio— sigue sin muestra. La línea base que heredamos
era 4 %. Al 2026-09-10.*

**`hardware`** · Una pantalla chica sobre el escritorio que muestra lo que está
pasando sin que la abras. El servidor renderiza, la pantalla dibuja, y cada
unidad en campo es un nodo más que el healer lee. Todavía es un prototipo:
la placa está elegida y verificada en un carrito local, el firmware compila
pero nunca corrió en la placa, y la caja es un DXF sin mediciones físicas.
*Cero señas. Hay una regla escrita antes de la primera compra: diez señas o no
hay lote. Al 2026-09-10.*

**`wisp`** · Mensajes y llamadas entre personas que se conocen, cifrados de
punta a punta, por un servidor chico que corre quien lo usa y no una empresa. La
cuenta es un par de claves que nace en tu dispositivo, sin teléfono ni email; a
alguien se lo agrega escaneando su QR y después comparan números de seguridad
en persona. Lo escribe Valen, de VT Security, y lo publica Legios.
*0.8, con llamadas, grupos chicos, varios dispositivos y copias cifradas.
Todavía sin revisión externa. Al 2026-10-05.*

**`night-line`** · Un juego para gente que no tiene atención, para tener al lado
de la terminal. Empezó el 2026-09-08 como una nave que volaba sola en la
terminal (título de trabajo: Wayfarer) y el 2026-09-23 se volvió otra cosa: un
tren en 3D, low-poly, que viaja entre estaciones-diorama. Armás el tren, suben
pasajeros, repartís carga para que crezcan cuatro pueblos, y el tren te espera
en cada parada; no hay apuro.
*La economía, los pueblos, las mejoras y el autoguardado andan, en Three.js.
Al 2026-09-24.*

**`ground-truth`** · Terror en primera persona sobre un hombre que trabaja desde
su casa etiquetando contenido como humano o generado, mientras algo se le mete
en la familia. Sutil hasta el último ítem.
*Preproducción en Godot 4: los doce días y los dos finales se juegan de punta a
punta en greybox. Falta escribir y dibujar los 401 ítems de la cola y las líneas
de las escenas. Al 2026-09-26.*

**`scout`** · La investigación de mercado para un estudio de juegos de Legios:
servidores de juegos, Roblox, portales web y la idea de un MMO, en cuatro
rondas. Es privado porque tiene planes de negocio y datos que no son nuestros.
*Nada está decidido: cada ronda termina con sus decisiones abiertas. Al
2026-10-16.*

**`app`** · La UI de Legios, rescatada entera de la versión anterior y atendida
por el servidor de `pipeline`. La regla es que no se reescribe: se tocan las
tablas de datos y la configuración, nunca un componente.
*Los 36 endpoints que pide la UI están declarados en el contrato. Al
2026-09-22.*

**`architecture`**, **`bitacora`** y **`web`** · Los ADR, los hallazgos y el
legajo del reinicio —por qué las cosas son como son—, el SOUL de la
organización con los handoffs de cada noche larga, y la landing.

## Cómo se conectan las tres del medio

Hay **un solo artefacto**, la spec, y todo lo demás la produce o la consume.
Es lo que hace que las piezas sean independientes y se conecten sin una
interfaz por cada par.

```mermaid
flowchart LR
    subgraph prod["Producen specs"]
        direction TB
        Healer["healer<br/>incidentes → causa raíz"]
        Clarify["clarify"]
        Reviewer["reviewer"]
        Drift["drift"]
    end

    Carto[("cartographer<br/>el mapa del repo")]

    Spec["<b>la spec</b><br/>el único artefacto"]

    Exec["el ejecutor<br/>externo, uno solo"]

    Carto -- "contexto citado" --> prod
    prod --> Spec
    Spec --> Gate{"revisión<br/>humana"}
    Gate --> Exec
    Exec --> PR["PR + verify: en verde"]
```

## Cómo trabajamos

Un hito no está terminado hasta que tiene tres cosas, y ninguna se negocia.

1. **Una demo que se corre y se ve.** Un comando, no una captura.
2. **Un gate de CI que vimos fallar antes de confiarle algo.** Si no podés
   mostrar el rojo, no tenés el gate. Ya pasamos tres meses con
   `continue-on-error: true` creyendo que teníamos uno.
3. **Un número comiteado.** En `numeros/`, con fecha y con el método al lado.

Y cada vía lleva una apuesta que puede perder, escrita antes de empezar. La del
healer, textual de su `SOUL.md`:

> Si los humanos rechazan la hipótesis de causa raíz agrupada más veces de las
> que la aceptan, agrupar no aporta nada y esto es un bot de error-a-issue.

Está redactada así a propósito. Dice cómo se vería que no funcione, que es lo
que hace que sea una apuesta y no una intención.

<details>
<summary><b>Los cuatro principios que se invocan a diario</b></summary>

<br>

Son tensiones, no eslóganes: cada uno decide una llamada ambigua.

1. **Memoria equivocada es peor que ninguna memoria.** Lo indetectable es
   `null`, no una suposición. Toda claim narrada lleva citas. Todo degrada a
   inspección viva, nunca por debajo.
2. **Ninguna capacidad se mergea sin su consumidor.** Si nadie la llama, no está
   terminada.
3. **Un gate se prueba fallando antes de confiar en él.** Tres meses de
   `continue-on-error: true` son tres meses de confianza construida sobre nada.
4. **Restringir el *qué*, liberar el *cómo*.** El contrato es el resultado, no
   el procedimiento.

</details>

<details>
<summary><b>Non-goals, cerrados</b> — cada uno es un error de v1 que no se repite</summary>

<br>

El detalle está en `docs/legajo-2026-08-14/03-ERRORES-Y-PRINCIPIOS.md`.

- **Ningún agente con protocolo propio.** El ejecutor es externo y es uno.
- **Ninguna infraestructura antes de que haya algo que hostear.** Las Fases A
  y B corrieron enteras local-first, `npx` y GitHub Actions. La infra de AWS
  recién entró en Fase C, cuando hubo algo real que aislar y algo real que
  servir.
- **Ningún conector más allá del primero de su clase.** v1 tuvo nueve
  conectores de tracker con cero uso.
- **Ningún dashboard** hasta que haya tráfico *y* una persona concreta que vaya
  a leer un panel concreto para contestar una pregunta concreta.
- **Ningún nombre de producto separado** para una parte de un producto. Las
  cosas se llaman por lo que hacen.

</details>

## Qué es público y qué no

El núcleo —cartographer, healer, pipeline— es propietario y sigue así. No hay
frontera open-core que mantener porque no hay producto abierto; se decidió el
2026-08-26.

Las herramientas son otra cosa. `quartermaster`, `archivist` y `tidbit` son
públicos y MIT porque no forman parte del producto: son cosas que hicimos para
nosotros, que le sirven a cualquiera, y que no revelan nada del núcleo. Ésa es
la regla, y no «todo abierto»: se publica lo que sirve suelto. Los juegos son un
caso aparte: Sun and Moon se juega gratis, pero el código queda adentro.

## Quiénes

Dos personas, y todo lo que hay acá lo escribimos entre los dos.

**Valentín Torassa** · [@ValentinTorassa](https://github.com/ValentinTorassa)<br>
**Sol Soletti** · [@solsolettidev](https://github.com/solsolettidev)

Founder-led y de operación privada. Si algo de acá te sirve, lo que se puede
usar hoy es [quartermaster](https://github.com/legiosai/quartermaster),
[archivist](https://github.com/legiosai/archivist),
[tidbit](https://tidbit.legios.com.ar/es/) y, para jugar de a dos,
[Sun and Moon](https://sunandmoon.legios.com.ar); lo demás todavía no sale del
taller.

<div align="center">
<br>
<sub>Construido por Valentín Torassa y Sol Soletti.</sub>
</div>
