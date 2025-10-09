# PRESENTE PASADO Y FUTURO 

## almacenamiento local en aplicaciones web

En sus inicios, las aplicaciones web enfrentaron grandes limitaciones en el almacenamiento local. Mientras las aplicaciones nativas podían guardar datos fácilmente mediante sistemas operativos, las web solo contaban con cookies, que resultaban poco seguras, lentas y con capacidad limitada (4 KB). La necesidad de un sistema más eficiente llevó al desarrollo de múltiples soluciones temporales, cada una con sus propias limitaciones.

---

## Antecedentes y evolución antes de HTML5

Durante los primeros años, surgieron varios métodos para intentar solucionar esta carencia:

userData (Internet Explorer): Permitía guardar hasta 64 KB por dominio usando XML, pero era exclusivo de IE.

Flash Local Shared Objects (Adobe): Introducidos en Flash 6, ofrecían 100 KB por dominio y requerían permisos adicionales para ampliar la capacidad.

Google Gears (2007): Introdujo una base de datos local basada en SQLite, ofreciendo almacenamiento ilimitado tras la aprobación del usuario.

Dojo Toolkit: Intentó unificar estas soluciones con una interfaz común, pero cada navegador tenía diferencias notables.

Estos métodos fueron considerados “hacks” porque dependían de plugins o navegadores específicos, sin una solución estandarizada.

---

## Nacimiento del almacenamiento HTML5


El Almacenamiento Web HTML5 solucionó los problemas anteriores al ofrecer una API estandarizada para guardar pares clave-valor de manera persistente, sin necesidad de complementos.
Ventajas principales:

Los datos no se envían al servidor, solo permanecen en el navegador.

Persisten tras cerrar pestañas o el navegador.

Es nativo, seguro y universal, compatible con navegadores modernos (IE8+, Firefox 3.5+, Chrome 4+, Safari 4+, Opera 10.5+, Android 2.0+).

El acceso se realiza mediante el objeto localStorage, que permite guardar, recuperar o eliminar datos fácilmente con métodos como setItem, getItem o removeIte.

---

## Seguimiento y gestión de cambios

HTML5 también permite detectar cambios en el almacenamiento mediante el evento storage, el cual notifica cuando se agregan, eliminan o modifican datos. Aunque no puede evitar los cambios, es útil para sincronizar información entre diferentes pestañas o ventanas del navegador.

---

## Limitaciones y consideraciones técnicas

Cada sitio web tiene un límite de 5 MB de almacenamiento por dominio.
Si se supera, se genera el error QUOTA_EXCEEDED_ERR. Actualmente, los navegadores no permiten solicitar más espacio mediante código, aunque algunos, como Opera, permiten al usuario ajustar la cuota manualmente.

Los datos se almacenan como cadenas de texto, por lo que los valores numéricos o booleanos deben convertirse con funciones como parseInt o parseFloat al recuperarlos.

---

## Ejemplo práctico: almacenamiento en un juego

El ejemplo del juego Halma demuestra el uso de localStorage para guardar el progreso del jugador (posición de piezas, movimientos, partida en curso, etc.).
Cuando el usuario cierra el navegador y regresa, los datos se restauran automáticamente, mostrando la utilidad real del almacenamiento HTML5 para mejorar la experiencia del usuario.
