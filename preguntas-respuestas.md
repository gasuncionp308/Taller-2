# Preguntas y respuestas del proyecto NutriBoost

## 1. ¿Qué propósito cumple cada etiqueta semántica principal de la página?

- `<header>`: contiene la cabecera, el logo y la navegación.
- `<nav>`: agrupa los enlaces de navegación hacia las secciones Menú y Beneficios.
- `<main>`: contiene el contenido principal de la página.
- `<section>`: divide el contenido en bloques temáticos: presentación, menú y beneficios.
- `<article>`: representa cada producto y cada beneficio de forma independiente.
- `<footer>`: muestra la información final y los derechos reservados.
- `<img>`: muestra las imágenes del hero y de los productos.
- `<a>`: permite navegar hacia las diferentes secciones.
- `<div>`: organiza visualmente elementos que no necesitan una etiqueta semántica específica.

La sección del cupón fue eliminada, por lo que actualmente la página contiene el hero, el menú, los beneficios y el footer.

## 2. ¿Qué variables del CSS se definieron, dónde se reutilizan y qué mejora aportan?

Las variables se encuentran en `variables.css`:

- `--primary-color`: color principal coral. Se usa en el hero, el logo y los precios.
- `--secondary-color`: color azul secundario. Actualmente está definido, pero ya no tiene un uso activo después de eliminar la sección del cupón.
- `--accent-color`: color amarillo usado en el badge, los botones principales y la sección de beneficios.
- `--dark-color`: color oscuro usado en textos y en el footer.
- `--light-color`: fondo claro y color de texto sobre fondos oscuros.
- `--font-main`: tipografía general del sitio.
- `--spacing-xs`, `--spacing-sm`, `--spacing-md` y `--spacing-lg`: controlan espacios, padding y separación entre elementos.
- `--border-radius`: controla los bordes redondeados de imágenes y botones.

Estas variables mejoran la consistencia visual y permiten cambiar colores, tipografía o espaciados desde un solo lugar sin modificar cada regla individualmente.

## 3. ¿Por qué se eligió Grid para una zona y Flexbox para otra?

Se utiliza **CSS Grid** en el hero para colocar el texto y la imagen en dos columnas cuando la pantalla es grande. Grid permite controlar filas y columnas de forma sencilla.

Las tarjetas de productos y beneficios utilizan el sistema de columnas responsive de Bootstrap, que está basado en una estructura de grid.

Se utiliza **Flexbox** para:

- Organizar verticalmente el contenido del hero.
- Colocar los botones en una fila.
- Distribuir los elementos internos de las tarjetas.
- Organizar la navegación.
- Alinear y separar elementos dentro de los diferentes bloques.

Flexbox es apropiado cuando los elementos se distribuyen principalmente en una sola dirección, horizontal o vertical.

## 4. ¿Qué regla pertenece al diseño móvil y qué cambia en cada breakpoint?

La regla principal para celulares es:

```css
@media (max-width: 767.98px)
```

En este breakpoint:

- La navegación se muestra como un menú colapsable mediante Bootstrap.
- Los enlaces de navegación tienen más espacio para facilitar el uso táctil.
- Los botones del hero permanecen en una fila.
- Ambos botones tienen un ancho flexible y equilibrado.
- Los botones tienen una altura mínima de `48px`.
- El texto de los botones no se divide en varias líneas.
- Se agrega separación entre los botones y la imagen del hero.
- Las tarjetas reciben más espacio interno.

El breakpoint de `600px` ajusta principalmente el padding del encabezado.

El breakpoint de `900px` cambia la distribución para pantallas grandes:

- El hero pasa a tener dos columnas.
- El título principal aumenta de tamaño.
- Las secciones tienen más espacio interno.
- El contenido se limita a un ancho máximo de `1200px`.
- El menú y la sección de beneficios se adaptan mejor al formato de escritorio.

Además, la clase `navbar-expand-md` de Bootstrap hace que la navegación se expanda desde tamaños medianos y permanezca colapsada en celulares.
