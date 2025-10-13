# MICRODATOS 

---

## Qué son los datos invisibles?

A veces en una página web se necesita guardar información que no se ve, pero que las máquinas o buscadores sí pueden leer.
Por ejemplo, datos de ubicación o coordenadas que el usuario no necesita ver.
HTML5 permite hacer esto usando datos invisibles, aunque se recomienda usar esta técnica solo cuando sea necesario, porque si alguien cambia el texto visible y olvida actualizar los datos invisibles, puede quedar desactualizado.
Un ejemplo sería poner las coordenadas de una empresa, pero sin mostrarlas directamente.
Esto se hace usando etiquetas como span y meta para guardar esa información en el código.
La ventaja es que esos datos ayudan a los bucadores a entender mejor la página y a mostrar información más precisa.

### *Cómo se anotan los datos invisibles*

Los datos invisibles se marcan con etiquetas especiales:

itemprop sirve para indicar qué tipo de información es.
itemscope y itemtype sirven para decir a qué grupo o “vocabulario” pertenece esa información.
Y meta se usa para guardar los valores sin que se vean.
Por ejemplo, si queremos agregar una latitud y longitud, usamos 
Aunque no se vea, el buscador puede leer esos números y saber que se trata de una ubicación.

## Marcar Eventos en HTML5

### *Qué son los microdatos de eventos*

HTML5 también permite marcar eventos (como conferencias, conciertos, reuniones, etc.) con microdatos.
Esto ayuda a que los buscadores como Google muestren la información más clara en los resultados, por ejemplo: el nombre del evento, la fecha, la ubicación y un enlace a la página.

### *Cómo se estructura un evento*

Cada evento se coloca dentro de una etiqueta <article> con atributos que indican que se trata de un evento, por ejemplo:

itemtype para decir que es un evento.

itemprop para indicar el tipo de dato (nombre, fecha, descripción, etc.).

Las partes importantes que se pueden marcar en un evento son:

Nombre del evento: se marca en el título.

Descripción: explica de qué trata.

Fechas y horas: se marcan con <time> usando atributos de fecha ISO.

Ubicación: puede incluir la dirección o una organización.

Foto: con el atributo de imagen.

URL: el enlace oficial del evento.

Cómo usan esto los buscadores

Cuando se usa correctamente, Google puede mostrar los eventos directamente en los resultados de búsqueda, como una tabla con fechas, lugares y nombres.
Por ejemplo, puede mostrar algo así:

Día del desarrollador de Google 2009 – Viernes 6 de noviembre – Centro de Congresos, Praga, República Checa.

Google incluso reorganiza los datos (como la fecha o la dirección) para que se vean más fáciles de leer.
