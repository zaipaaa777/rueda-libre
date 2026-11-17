Descripción del proyecto

Mi proyecto es Rueda Libre, un sitio web para un negocio de alquiler de bicicletas en Medellín. Tiene dos productos conectados entre sí, y ambos están publicados en GitHub Pages desde el mismo repositorio.

1. Sitio principal (v2.0, hecho con Bootstrap)

Tiene tres páginas: index.html, paginas/reservas.html y paginas/tarifas.html, con los estilos en css/styles.css.
Incluye una navbar responsive, un carrusel de promociones (2x1, 20 % de descuento en eléctricas, cumpleañeros y ahora Rueda Nocturna), tablas de tarifas, cards de flota y rutas, un formulario de reservas con validación de Bootstrap, alertas y un modal de políticas.
Le di identidad de marca propia sobre Bootstrap con variables --bs-*, el botón btn-naranja, clases personalizadas y Bootstrap Icons. Lo hice porque el cliente dijo que la versión beta “parecía mil sitios”.

2. Landing Rueda Nocturna (hecha con Tailwind CSS, en la carpeta nocturna/)

Es el producto nuevo: recorridos guiados en bicicleta de noche, de jueves a sábado a las 7:30 p. m.
La construí con Tailwind CLI usando solo clases de utilidad. Los colores y fuentes de marca están definidos en @theme (azul-noche, crema, naranja-pedal, amarillo-farol, font-titulos, font-texto) y tiene modo oscuro.
Sus secciones son el hero, las tres rutas (Fácil, Medio y Difícil), los planes (Individual, Pareja como “Más elegido” y Grupo), cómo funciona, el formulario de inscripción y el pie de página. También tiene un kit de componentes (botón, card, alerta e input) en componentes.html.
Se conecta con el sitio de Bootstrap por la navbar, el carrusel, el logo y el botón “Reserva tu bici”.
Mi recomendación de framework

Recomiendo usar Astro con Tailwind, y lo digo por los problemas reales que me encontré en el proyecto:

Problema que tengo hoy	Cómo lo resuelve Astro
La navbar y el pie están copiados en cada página (para agregar un solo enlace tuve que editar tres archivos)	Escribo un componente Navbar y un Layout una sola vez
Los colores y fuentes de marca están duplicados (--bs-* y @theme)	Tengo un solo sistema de diseño
Los precios y las rutas están escritos a mano dentro del HTML	Los guardo como datos y los recorro para generar las cards
Dos frameworks de CSS cargan el doble de estilos	Con el tiempo lo unifico todo en Tailwind
