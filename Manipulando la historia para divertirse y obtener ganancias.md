# Manipulando la historia para divertirse y obtener ganancias

---

## Qué es la API de historial de HTML5

La API de historial de HTML5 es una herramienta que permite modificar el historial del navegador mediante scripts, sin necesidad de recargar toda la página.
Antes, cuando cambiabas una URL, el navegador tenía que recargar todo el sitio, incluso si solo cambiaba una pequeña parte del contenido. Con esta nueva función, puedes cambiar la URL visible, añadir o quitar entradas en el historial, y detectar cuándo el usuario presiona el botón de “Atrás”, sin actualizar toda la página.
Esto es muy útil en aplicaciones web que funcionan con mucho código JavaScript, ya que mantiene las URL funcionales y únicas, incluso cuando la página no se recarga.

### Por qué se creó esta API

Durante muchos años, los desarrolladores web crearon trucos para evitar recargar las páginas, pero eso hacía que las URL dejaran de ser útiles.
Por ejemplo, si una aplicación cargaba todo su contenido dentro de una sola página, la barra de direcciones no cambiaba, lo que significaba que no podías compartir el enlace, ni marcarlo, ni indexarlo correctamente en buscadores.

La API de historial soluciona ese problema:

Permite mantener una URL diferente para cada parte o vista de la aplicación.

Evita recargar toda la página.

Mejora la velocidad, eficiencia y experiencia del usuario.

En pocas palabras: hace que las páginas parezcan moverse, pero sin moverse de verdad.

### Cómo funciona la API de historial

*La idea básica*

Imagina que tienes dos páginas, A y B, y que son casi iguales (el 90% es lo mismo).
Con la API de historial puedes hacer que el usuario pase de A a B sin recargar todo.
El proceso es así:

Cargas solo la parte nueva (el 10% diferente), usando una petición con código (como XMLHttpRequest).

Cambias el contenido visible con lo que descargaste, sin recargar.

Actualizas la URL con la dirección de la nueva página, pero sin salir de la actual.

El resultado: el usuario cree que navegó a otra página, pero en realidad todo pasó dentro de la misma.

*La ilusión del cambio*

Este método da la ilusión de navegación real.
Por ejemplo, el navegador muestra la URL de la página B, pero nunca se cargó desde el servidor.
Solo cambió el contenido y la dirección visible.
Así, la experiencia es más rápida, sin interrupciones y con menos consumo de datos.

Pero eso sí: lograr esta “ilusión” requiere programar bien los pasos y coordinar los cambios de contenido con el historial del navegador.
