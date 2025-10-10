# *UNA FORMA DE LOCURA*

Este capítulo explica cómo HTML5 mejoró mucho los formularios web. Antes, solo había campos simples como texto, contraseñas o botones. Ahora, con HTML5 existen muchos nuevos tipos de entrada que hacen más fácil y moderna la interacción con los formularios, sin necesidad de usar tanto JavaScript ni trucos complicados

## placeholder

HTML5 permite poner un texto dentro de los campos vacíos para dar una pista de lo que se debe escribir.
Ese texto desaparece al hacer clic o al empezar a escribir.
Si el navegador no lo entiende, simplemente lo ignora, así que **no genera errores.**
No se puede usar HTML dentro del texto del marcador, solo texto simple.

## autofocus

Con este atributo, un campo puede activarse solo al cargar la página, sin usar JavaScript.
Antes, esto se hacía con scripts que a veces causaban molestias porque robaban el foco o interrumpían al usuario.
El nuevo método es más limpio y permite que los navegadores lo manejen mejor.
Si el navegador no lo admite, se puede combinar con un pequeño script para mantener compatibilidad

## Nuevos tipos de campos

*1. Direcciones de correo electrónico*

El campo type="email" verifica que el texto tenga formato de correo (por ejemplo, con “@”).
En dispositivos como el iPhone, el teclado cambia para mostrar teclas especiales como “@” y “.com”, haciendo más cómodo escribir correos.
En navegadores antiguos, funciona igual que un campo de texto normal, así que no hay problema en usarlo.

*2. Direcciones web*

El campo type="url" sirve para introducir direcciones de páginas.
También cambia el teclado en móviles y mejora la validación del texto.
En navegadores de escritorio se ve como un campo normal, pero valida automáticamente que la dirección sea válida.

*3. Números*

El tipo type="number" permite ingresar solo valores numéricos y definir un mínimo, máximo y pasos (por ejemplo, de 2 en 2).
En algunos navegadores aparece con flechas para subir o bajar el valor, y en móviles se activa un teclado numérico.
En los que no lo soportan, se comporta como texto sin problema.

*4. Controles deslizantes rango*

Con type="range", el usuario puede mover una barra para elegir un número dentro de un rango.
Es visual, rápido y útil para configuraciones como volumen, brillo o edad.
En algunos navegadores se ve como un control deslizante; en otros, como texto normal.

*5. Selectores de fecha y hora*

HTML5 incluye campos como type="date", "month", "week", "time", etc., que permiten seleccionar fechas fácilmente.
Opera fue el primer navegador en soportarlos.
En otros, se comportan como texto, pero se pueden combinar con bibliotecas externas como jQuery UI o Dojo para lograr el mismo efecto.

*6. Cuadros de búsqueda*

El tipo type="search" se usa para los buscadores de páginas.
En Safari y Chrome se ve con esquinas redondeadas y una “x” para borrar el texto, dando un toque moderno.
En otros navegadores funciona como texto, pero ya es recomendable usarlo para mantener buenas prácticas.

*7. Selector de color*

El tipo type="color" permite elegir un color desde una paleta y devuelve su valor hexadecimal.
Opera fue el primero en implementarlo, y es útil para herramientas que permiten personalizar colores sin escribir códigos.

## Validación automática

HTML5 puede verificar automáticamente que los datos sean correctos sin usar JavaScript.
Por ejemplo, si un correo no tiene el formato correcto, el navegador muestra un mensaje de error.
También valida URLs o números fuera de rango.
Si no se desea esta validación, se puede desactivar con el atributo novalidate.
Esto reduce errores y mejora la experiencia del usuario.

## Campos obligatorios

Con el atributo required, se puede hacer que un campo sea necesario antes de enviar el formulario.
Si no se llena, el navegador mostrará una alerta o resaltará el campo.
Esto evita enviar formularios incompletos sin tener que usar scripts adicionales.
