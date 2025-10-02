# CANVAS

---

canvas es un lienzo en blanco en el que se pueden dibujar gráficos, formas, texto e imágenes mediante JavaScript.
No tiene contenido ni borde por defecto; se puede añadir un id para acceder fácilmente desde el DOM.
Se pueden usar múltiples lienzos en la misma página, cada uno con su propio contexto de dibujo getContext"2d".
---

## Dibujo básico de formas

Métodos principales: fillRect() para rectángulos rellenos, strokeRect() para bordes, clearRect() para limpiar
Propiedades: fillStyle (color de relleno), strokeStyle (color de borde).
Cambiar ancho o alto del canvas restablece el lienzo y sus propiedades.

---

## Coordenadas del lienzo

Sistema de coordenadas 2D: (0,0) es la esquina superior izquierda, X aumenta hacia la derecha y Y hacia abajo.
Se pueden dibujar líneas con rutas usando moveTo() y lineTo(), y luego trazarlas con stroke().

---

## Texto en canvas

Atributos de fuente: font, textAlign, textBaseline.
fillText(text, x, y) dibuja el texto en la posición deseada.
Se pueden usar líneas base como top, middle, bottom, y tamaños de fuente relativos.

---

## Gradientes

Se pueden crear degradados lineales o radiales (createLinearGradient y createRadialGradient).
Se definen colores en posiciones entre 0 y 1 con addColorStop
Para dibujar un degradado se asigna a fillStyle y se rellena una forma.

---

## Imágenes en canvas

drawImage() permite dibujar imágenes ya sea completas, escaladas o recortadas.
Es importante asegurarse de que la imagen esté completamente cargada (onload) antes de dibujarla.

Ejemplo: dibujar múltiples imágenes escaladas para efectos de mosaico o sprites.

Ventaja: permite combinar texto, formas e imágenes en un solo lienzo de forma dinámica.

---

## Compatibilidad con Internet Explorer

IE < 9 no soporta canvas nativamente; se puede usar ExplorerCanvas (excanvas.js).
Limitaciones: solo degradados lineales, patrones repetidos, no se soportan regiones de recorte ni escalado complejo, y rendimiento más lento.
Es recomendable ejecutar todo el código canvas después del evento onload para evitar errores de inicialización.

---

## Ejemplo completo: juego Halma en canvas

Juego de tablero 9×9 con piezas que se mueven a celdas vacías o saltando sobre otras piezas.
Inicialización: establecer dimensiones del <canvas> y obtener contexto de dibujo.
Uso de eventos: addEventListener("click", halmaOnClick) para detectar clics y calcular la posición relativa al canvas.
Dibujo del tablero: líneas verticales y horizontales, trazado completo cada vez que cambia el estado.
Dibujo de piezas: círculos usando arc(), rellenos opcionales si la pieza está seleccionada.
Lógica de juego: control de movimientos válidos, selección de piezas y seguimiento del progreso

---

## Conclusión

<canvas> permite crear gráficos, texto, imágenes y juegos interactivos dentro de una página web.
Es flexible y poderoso, pero requiere conocer coordenadas, contexto de dibujo, rutas, fuentes y eventos de usuario.
Se puede usar en combinación con librerías externas para compatibilidad con navegadores antiguos.
