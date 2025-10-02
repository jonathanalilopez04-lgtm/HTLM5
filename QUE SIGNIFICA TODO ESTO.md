# ¿ QUE SIGNIFICA TODO ESTO ?

---

## Diferencias entre HTML4 y HTML5 en encabezados

En HTML4 los títulos iban del h1 al h6 y solo podía existir un h1 en todo el documento. Esto era un problema en páginas grandes o hechas con plantillas, porque obligaba a ajustar manualmente los niveles de los títulos
En HTML5 aparece un nuevo sistema: cada sección, como un artículo o una sección, puede tener su propio h1 sin romper el esquema del documento. Cada vez que se abre una sección nueva, se crea un nodo independiente en la jerarquía. Esto permite copiar y pegar un artículo completo dentro de otra página sin tener que modificar los encabezado
La ventaja principal es que facilita mucho la organización del contenido y la reutilización de bloques completos en distintas partes de un sitio.

---

## El uso del encabezado o header

El elemento header se utiliza para agrupar el contenido de la cabecera de una página o de un artículo. Allí se suelen colocar el título, la fecha de publicación u otra información relacionada con el inicio de esa sección.
Lo importante es que no se limita solo a la cabecera principal de la página, sino que también puede estar dentro de cada artículo o sección.

---

## El elemento time para fechas 

Antes las fechas se ponían como un simple párrafo con una clase, lo cual no tenía un valor semántico claro. Con HTML5 aparece el elemento time, que sirve para indicar fechas y horas de manera comprensible tanto para las personas como para las máquinas.
Este elemento puede contener tres cosas:

Una fecha legible por máquina gracias al atributo datetime.

Una fecha u hora visible para los usuarios.

Una marca opcional que indica si corresponde a la fecha de publicación de un artículo o de todo el documento.

El uso de este elemento permite que buscadores, navegadores y lectores de pantalla entiendan con mayor precisión cuándo se publicó un contenido o a qué fecha corresponde cierta información.

---

## El elemento nav para la navegación

En páginas más antiguas la navegación del sitio se ponía dentro de un div, acompañado de listas de enlaces. Aunque funcionaba, no quedaba claro que eso correspondía a la navegación principal del sitio.
Con HTML5 se usa el elemento nav, que indica de forma semántica que ese bloque corresponde a la barra de navegación.
Esto mejora la accesibilidad porque permite que los usuarios con discapacidades puedan saltar directamente a la barra de navegación o ignorarla si lo desean. También ayuda a los buscadores y programas lectores de pantalla a entender mejor la estructura de la página.
Aunque aún se recomienda mantener enlaces de salto para accesibilidad, el nav poco a poco los reemplaza de manera natural.

---

## El elemento footer

En HTML4 lo común era marcar el pie de página con un div llamado “footer”. Ahora existe un elemento específico que se llama footer, pensado justamente para esa función.

En un footer se suele incluir información como:

Derechos de autor.

Información de contacto.

Enlaces a secciones secundarias como privacidad, términos, ayuda o páginas de autor.

Dependiendo del sitio, el footer puede ser muy simple o contener varias secciones completas con navegación adicional. Por ejemplo, sitios como Google o CNN incluyen en el pie enlaces de privacidad, contacto y servicios. En los blogs es común ver un footer con enlaces a otros proyectos del autor.

---

## *Conclusión* 

HTML5 introdujo mejoras importantes en la semántica del código. Gracias a los nuevos elementos como header, time, nav y footer, las páginas son más claras, fáciles de mantener y mucho más accesibles para todos los usuarios.
Estos cambios representan un avance respecto a HTML4, donde era necesario usar divs genéricos y clases personalizadas para organizar la estructura. Ahora, con elementos específicos, el código tiene un sentido más lógico y ordenado.
