# Detectando las funciones de HTML5

HTML5 no es una sola cosa, es un conjunto de funciones nuevas que los navegadores pueden o no soportar. Por eso no tiene ##sentido decir “mi navegador soporta HTML5” en general; lo correcto es revisar función por función, como video, canvas, geolocalización y otras.
Para saber si un navegador soporta algo, se usan técnicas que revisan si ciertos objetos o propiedades existen. Cuando un navegador muestra una página web, crea algo llamado DOM, que es como un mapa de todos los elementos de la página: párrafos, divs, imágenes, videos, etc. Cada objeto en el DOM puede tener propiedades únicas que indican si soporta ciertas funciones de HTML5.

---

## Técnicas para detectar funciones

Hay cuatro formas básicas de comprobar si algo funciona en un navegador:

Revisar si existe una propiedad en un objeto global, como window o navigator. Por ejemplo, para ver si soporta geolocalización.
Crear un elemento y revisar si tiene una propiedad especial. Por ejemplo, para ver si soporta canvas.
Crear un elemento, revisar si tiene un método y probar qué devuelve. Por ejemplo, para saber qué formatos de video soporta.
Crear un elemento, ponerle un valor y ver si lo mantiene. Por ejemplo, para saber qué tipos de campos de formulario input soporta.

---

## Modernizr

Modernizr es una librería gratuita de JavaScript que detecta muchas funciones de HTML5 y CSS3. Solo se incluye en la página y automáticamente crea un *objeto llamado Modernizr que tiene propiedades verdaderas o falsas según lo que soporte el navegador*.
Por ejemplo, si el navegador soporta canvas, Modernizr.canvas será verdadero; si no, será falso. Así puedes decidir si usar una función o mostrar otra alternativa.

---

## Canvas

El canvas es como un lienzo donde se puede dibujar lo que quieras usando JavaScript: gráficos, juegos, animaciones, etc.
Incluso hay una parte del canvas solo para texto, porque no todos los navegadores incluyen estas funciones al principio.

---

## Video

HTML5 tiene un nuevo elemento video que permite poner videos en la página sin plugins como Flash o QuickTime. Los navegadores que soportan video eligen automáticamente qué formato reproducir.

Hay diferentes formatos de video:

H.264:**usado en Safari y iPhone, requiere licencia**.
Ogg Theora + Vorbis: usado en Firefox y Chrome, es libre.
WebM: nuevo, libre y abierto, funciona en Chrome, Firefox y Opera.
HTML5 permite que aplicaciones web funcionen sin conexión a internet. Primero se descargan todos los archivos necesarios y luego, aunque estés desconectado, puedes seguir usando la aplicación. Cuando vuelves a estar online, los cambios se sincronizan.

---

## Almacenamiento local

HTML5 permite guardar información en la computadora del usuario sin usar cookies. Esto es más rápido y permite almacenar más datos. Solo los sitios pueden leer sus propios datos, nadie más puede tocarlos.

---

## Web Workers

Los web *workers permiten que JavaScript se ejecute en segundo plano, como hilos que corren al mismo tiempo que la página principal*. Esto es útil para cálculos complejos o cargar datos sin que la página se trabe.

---

## Aplicaciones offline

HTML5 permite que aplicaciones web funcionen sin conexión a internet. Primero se descargan todos los archivos necesarios y luego, aunque estés desconectado, puedes seguir usando la aplicación. Cuando vuelves a estar online, los cambios se sincronizan.

---

## Geolocalización

HTML5 permite saber dónde estás usando diferentes métodos: *IP, Wi-Fi, torres de celular o GPS*. Si el navegador lo soporta, puede usar estas funciones; si no, hay plugins o APIs antiguas que pueden ayudar.

---

## Tipos de entrada

HTML5 añadió muchos tipos nuevos de campos en los formularios:

search: cajas de búsqueda

number: números con flechitas

range: deslizadores

color: selector de colores

tel, url, email: teléfono, direcciones web y correo

date, month, week, time, datetime-local: fechas y horas

Esto permite crear formularios más inteligentes y fáciles de usar.

---

## Texto de marcador (placeholder)

El placeholder es el texto que aparece dentro de un campo mientras está vacío y desaparece cuando escribes.

---

## Autofocus

El autofocus permite que un campo se enfoque automáticamente al abrir la página, lo que es útil para buscadores o formularios, pero puede molestar a algunos usuarios.

---

## Microdatos

Los microdatos sirven para añadir información extra a tu página que los buscadores pueden leer. Por ejemplo, marcar que una foto tiene licencia Creative Commons.

---

## Historial

HTML5 permite manejar el historial del navegador desde JavaScript, agregando entradas y reaccionando cuando el usuario usa el botón de retroceso. Esto es útil para aplicaciones que cambian de pantalla sin recargar la página.

---

## *Resumen* 

HTML5 es un conjunto de funciones nuevas que los navegadores pueden soportar o no. Para usarlo de forma segura:

Detecta qué funciones soporta el navegador.

Usa herramientas como Modernizr para facilitar la detección.

Ten soluciones alternativas si algo no está soportado.

Con esto puedes hacer páginas más modernas con videos, gráficos, formularios inteligentes, almacenamiento local y hasta aplicaciones que funcionen offline.
