# - VAMOS A DEJAR ESTO ALADO


## Aplicaciones web sin conexión

Una aplicación web sin conexión es una página o sitio que puede funcionar aunque no tengas Internet. Suena raro, porque normalmente una página se descarga desde la red, pero con HTML5 esto es posible. Lo que hace el navegador es guardar ciertos archivos (como el HTML, el CSS, las imágenes y el JavaScript) para poder usarlos después sin conexión.
Cuando visitas por primera vez la aplicación, el navegador descarga todo y lo guarda. Luego, si entras sin Internet, usa esos archivos guardados para mostrar la página igual.
El desarrollador tiene que encargarse de que la app funcione bien tanto conectada como desconectada. Por ejemplo, si la app guarda información, debe hacerlo localmente mientras no hay conexión y sincronizarla después con el servidor cuando regrese el Internet.

### El archivo de manifiesto

El corazón de una aplicación sin conexión es un archivo de manifiesto, que básicamente es una lista de los recursos que la app necesita para funcionar sin Internet. Este archivo le dice al navegador qué debe guardar.
Por ejemplo, puede tener una lista con cosas como:
Un archivo de estilos (CSS)
Un archivo de código (JavaScript) Imágenes o sonidos Cuando el navegador lee el manifiesto, descarga todo eso y lo almacena localmente. Así, si pierdes conexión, la app puede seguir funcionando igual.
Cada página de la aplicación debe tener una referencia al archivo de manifiesto. Si solo hay una página, basta con ponerlo en esa; pero si hay varias, cada una debe apuntar al mismo manifiesto para que todas estén disponibles sin conexión.

### Tipos de secciones en el manifiesto

*CACHE*: Aquí se ponen los archivos que deben guardarse para usarse sin conexión.

*NETWORK*: Aquí van los archivos que no deben guardarse, como los que se actualizan siempre en línea (por ejemplo, un contador de visitas).

*FALLBACK*: Aquí se indican archivos de reemplazo por si algo falla o no se encuentra. Por ejemplo, si intentas abrir una página y no está guardada, puede mostrarse un mensaje o una página especial que diga “sin conexión”.

Esto sirve, por ejemplo, para sitios grandes como Wikipedia, donde sería imposible guardar todo. Pero se puede hacer que solo las páginas que visitas se guarden automáticamente. Así, aunque no tengas Internet después, las páginas que ya abriste sí estarán disponibles.

### Cómo funciona todo el proceso

Cuando el navegador detecta que una página tiene un archivo de manifiesto, empieza una serie de pasos automáticos:

Comprueba si el manifiesto es nuevo o ya lo tiene guardado.

Si es nuevo, descarga todos los archivos y los guarda.

Si ya lo tenía, revisa si ha cambiado algo.

Si no cambió, no hace nada.

Si sí cambió, descarga de nuevo los recursos.

Si ocurre algún error (por ejemplo, si un archivo no se puede descargar), todo el proceso falla y no se guarda nada.

Esto puede ser muy frustrante para los desarrolladores porque a veces un solo archivo daña todo. Además, el navegador a veces guarda los archivos en su propia caché y no revisa si hay actualizaciones, lo que puede causar confusión al probar los cambios.

Una forma de evitar eso es desactivar la caché del servidor o cambiar el número de versión en el archivo de manifiesto cada vez que se hace una actualización. Así, el navegador nota que hay algo nuevo y vuelve a descargar los archivos.

### Ejemplo sencillo

Imagina que tienes un juego hecho en HTML5 llamado Halma.
Para que funcione sin conexión, creas un archivo de manifiesto donde pones los archivos que necesita el juego, como el HTML principal y el archivo JavaScript del juego.

Cuando el usuario entra por primera vez, el navegador guarda esos archivos. Luego, aunque se quede sin Internet, puede seguir jugando sin problemas, porque el juego ya está guardado en su dispositivo. Además, como el juego recuerda su estado localmente, puede continuar donde lo dejó.
