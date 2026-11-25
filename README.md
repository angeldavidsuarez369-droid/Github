# Proyecto Final — Café Altiplano

## 1. Mapa del sitio
- **index.html**: portada de Café Altiplano con presentación general, botón de acceso a reservas y cita destacada.
- **carta.html**: índice con anclas internas (`#bebidas`, `#metodos`) y tabla de precios estructurada con `caption`, `thead`, `tbody` y `th`.
- **sedes.html**: presentación de sede con imagen (`figure` y `figcaption`), ficha de datos (`dl`) y listas (`ul` y `ol`).
- **reservas.html**: formulario de reservas con `fieldset`, `legend`, etiquetas `label`, `select`, botones `radio`, `checkbox`, `textarea` y campos obligatorios.

## 2. Tabla de medidas

| Página | 500 px | 800 px | 1200 px |
|---|---|---|---|
| index | 1 columna, sin scroll | 2 columnas, sin scroll | 3 columnas, sin scroll |
| carta | 1 columna, sin scroll | 2 columnas, sin scroll | 3 columnas, sin scroll |
| sedes | 1 columna, sin scroll | 2 columnas, sin scroll | 3 columnas, sin scroll |
| reservas | 1 columna, sin scroll | 2 columnas, sin scroll | 3 columnas, sin scroll |

## 3. Justificación de cinco unidades
1. **rem** (en tamaños de letra y espaciados): permite escalar de manera uniforme respecto al tamaño raíz (`html { font-size: 100% }`) y respeta la configuración de lectura del usuario.
2. **ch** (en `max-width: 65ch` en los párrafos): limita el ancho de las líneas de texto a unos 65 caracteres para facilitar la lectura.
3. **%** (en `width: 100%` en tablas y galería): adapta el ancho del elemento al espacio disponible de su contenedor padre.
4. **vh** (en `min-height: 45vh` de la portada): ajusta la altura mínima del bloque principal de forma proporcional al alto de la pantalla.
5. **px** (solo en bordes finos de `1px` y `2px`): mantiene líneas nítidas y consistentes sin deformarse al cambiar el tamaño de fuente.

## 4. Decisiones
Se utilizó un enfoque **móvil primero** (*Mobile First*) porque la mayoría de los clientes consulta el sitio desde su teléfono, partiendo de una estructura base de una columna. Los puntos de ruptura de **600 px** y **900 px** permiten reorganizar el contenido progresivamente en 2 y 3 columnas mediante CSS Grid.

## 5. Dificultades
Evitar que las tablas y las imágenes generaran desplazamiento horizontal en pantallas pequeñas fue el principal reto; se solucionó aplicando `box-sizing: border-box`, imágenes flexibles (`max-width: 100%; height: auto`), un contenedor con `overflow-x: auto` para la tabla y `gap` en lugar de márgenes sueltos.
## Examen 2

### 1. Qué agregaste y hojas CSS modificadas
Se agregó la página `nosotros.html` con portada, índice con anclas internas, línea de tiempo ordenada (`ol`), tarjetas del equipo, cita con `blockquote` y `cite`, lista de valores (`ul`), tabla de cifras (`table`), glosario (`dl`) y formulario «Escribinos», además de enlazar **Nosotros** en el menú de las cinco páginas. Se actualizaron `css/tipografia.css`, `css/cajas.css`, `css/componentes.css` y `css/layout.css`.

### 2. Tabla de medidas (`nosotros.html`)

| Página | 500 px | 800 px | 1200 px |
|---|---|---|---|
| nosotros | 1 columna, sin scroll | 2 columnas, sin scroll | 3 columnas, sin scroll |

### 3. Tres medidas y escala tipográfica
- **Escala tipográfica en `rem` (`2.25rem` / `1.75rem` / `1.25rem` / `1rem`)**: mantiene una jerarquía clara entre `h1`, `h2`, `h3` y texto base sin usar `px` en fuentes.
- **`max-width: 65ch` en párrafos y `55ch` en la cita**: controla el ancho de lectura para que las líneas no resulten cansadas.
- **`min-height: 45vh` en la portada**: adapta la altura mínima del bloque inicial según el alto de la ventana.

### 4. Dificultad y solución
Al combinar un fondo oscurecido con gradiente y texto claro sobre la portada en distintos tamaños de pantalla, el reto fue mantener buen contraste y evitar desbordes horizontales; se resolvió usando capas semitransparentes en `rgba` desde `:root`, `gap` en el Grid y `width: 100%` con `box-sizing: border-box`.