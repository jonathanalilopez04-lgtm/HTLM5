# Compatibilidad y Distribución de Vídeo

---

## Múltiples Formatos de Vídeo

Para garantizar que los vídeos se reproduzcan en la mayor cantidad posible de navegadores y dispositivos, es recomendable codificar el mismo contenido en tres formatos distintos:

Ogg (.ogv) con códecs Theora y Vorbis.

MP4 (.mp4) con códec H.264 para vídeo y AAC para audio.

WebM (.webm) con códec VP8 para vídeo y Vorbis para audio.

Cada navegador seleccionará automáticamente la primera fuente que pueda reproducir, evitando descargas innecesarias y optimizando el ancho de banda. Esta técnica asegura que los visitantes obtengan la versión del vídeo compatible con su navegador sin interrupciones.

---

## Respaldo para Navegadores

Aunque HTML5 ofrece un estándar moderno para la reproducción de vídeo, muchos navegadores antiguos no soportan todos los elementos del video. Por ello, es importante proporcionar un respaldo en Flash, mediante un reproductor como FlowPlayer.
Este método permite que los navegadores antiguos que no soportan HTML5 puedan reproducir los vídeos correctamente. Los navegadores modernos simplemente ignorarán el elemento de Flash, mientras que los antiguos lo usarán como alternativa, garantizando compatibilidad universal.

---

## Tipos MIME y Configuración del Servidor

Los tipos MIME son esenciales para que los navegadores identifiquen correctamente el formato de los archivos de vídeo. Configurar correctamente el tipo MIME evita que los vídeos se reproduzcan localmente pero fallen al ser publicados en un servidor.

.ogv - video/ogg

.mp4 - video/mp4

.webm - video/webm

En servidores Apache, esto se puede configurar mediante la directiva AddType en el archivo .htaccess. Otros servidores web requieren configuraciones similares para asegurar que los navegadores interpreten los vídeos correctamente.

---

## Compatibilidad con Dispositivos Móviles

*iOS (iPhone y iPad)*

Versiones antiguas (iOS 3.x) no reconocen vídeos que no sean el primer formato listado.

Los dispositivos solo reproducen MP4 con H.264 y AAC correctamente.

El atributo poster puede generar problemas en versiones anteriores a iOS 4.

*Android*

Versiones anteriores a 2.3 no reconocen correctamente el atributo type de los <source>.

Solo los archivos MP4 con extensión .mp4 son reconocidos.

Los controles del vídeo no se muestran, por lo que es necesario proporcionar interfaz de reproducción manual, por ejemplo con un clic sobre el vídeo.

Estas consideraciones aseguran que, incluso en dispositivos antiguos, el contenido de vídeo sea accesible y reproducible.

---

## Controles y Reproducción Automática

*HTML5 permite utilizar atributos como controls, preload y autoplay:*

controls: muestra controles predeterminados para reproducir, pausar o ajustar el volumen.

preload: indica si el vídeo debe descargarse al cargar la página (auto, metadata, none).

autoplay: reproduce automáticamente el vídeo al cargar la página, aunque en móviles puede estar restringido.

Además, se puede utilizar JavaScript para controlar manualmente la reproducción, garantizando compatibilidad en dispositivos que no soportan el autoplay de manera nativa.

---

## Conclusión: Reproducción Universal

Combinando HTML5 y Flash, múltiples formatos de vídeo, configuración correcta de tipos MIME y consideraciones específicas para móviles, se logra un sistema de reproducción de vídeo robusto y universal. Esta estrategia asegura que todos los usuarios, sin importar el navegador, dispositivo o sistema operativo, puedan acceder al contenido de manera fluida, optimizando la experiencia y el uso de ancho de banda.
