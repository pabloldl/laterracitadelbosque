# La Terracita del Bosque

Rediseño visual completo del 30/10/2026. Web estática en HTML5, CSS3 y JavaScript vanilla, sin compilación. Abrir `index.html` con Live Server. Solo se ha trabajado dentro de `la-terracita-del-bosque/`. Sin commits, pushes ni despliegues.

## Diseño y contenido

Nueva portada fotográfica con título contenido superpuesto en escritorio y una composición independiente en móvil: foto, presentación y botón. Paleta blanco roto, azul petróleo, arena y terracota; nueva marca, menú móvil desplegable, presentación breve, sección del entorno y cierre compacto de ubicación y reservas. No se conserva la anterior composición de gran titular sobre una fotografía ni sus secciones numeradas.

Solo se confirman nombre, actividad y localidad proporcionados por el usuario: La Terracita del Bosque, alojamiento turístico, 11670 El Bosque, Cádiz. El usuario ha incorporado cuatro fotografías reales autorizadas de la propiedad. Se muestran una vez cada una: terraza en portada y salón, dormitorio y vistas en la galería. No se inventan capacidad, instalaciones, servicios, precios, horarios, reseñas, teléfono ni dirección exacta.

Reserva externa exclusivamente mediante https://www.booking.com/hotel/es/la-terracita-del-bosque.es.html . La consulta del 29/10/2026 encontró una verificación antirrobots; no se han podido verificar las características de la propiedad ni el proceso externo de reserva. Ambos botones mantienen la URL canónica, sin seguimiento.

Entorno: https://www.cadizturismo.com/municipios/el-bosque . Fuente oficial consultada en la creación inicial para calles blancas, fuentes, río Majaceite, valles y jardín botánico El Castillejo. No son servicios ofrecidos por el alojamiento. El enlace al mapa sitúa únicamente la localidad.

## Fotografías y licencias

Se conserva el río Majaceite como imagen ilustrativa del entorno. La panorámica anterior permanece en disco para conservar el recurso y sus créditos, pero ya no se muestra. Las cuatro fotografías de la propiedad proceden del usuario.

- `imgs/el-bosque-sierra.jpg`: **El Bosque Lomo de Enmedio.JPG**, Antonio Acosta Fernández. Versión de 1920 px. Fuente: https://commons.wikimedia.org/wiki/File:El_Bosque_Lomo_de_Enmedio.JPG . Licencia CC BY 3.0: https://creativecommons.org/licenses/by/3.0/ . Metadatos de autoría y licencia conservados en `imgs/source-metadata.json`. Redimensionado y recorte visual de presentación.
- `imgs/rio-majaceite.jpg`: **Majaceite.jpg**, El Pantera. Versión de 1280 × 960 px. Fuente y licencia comprobadas el 30/10/2026: https://commons.wikimedia.org/wiki/File:Majaceite.jpg . Licencia seleccionada CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/ . Imagen redimensionada, sin filtros de color ni recortes. Se conserva CC BY-SA 4.0 para esta versión de la fotografía. No se aplica esa licencia al resto de la web.

Créditos, fuentes y enlaces a las licencias disponibles en el desplegable del pie. Comparadas mediante SHA-256 con las imágenes accesibles de los otros proyectos, excluyendo carpetas de pruebas `.qa/`: no hay coincidencias binarias. Esto no detecta versiones con distinta compresión o resolución.

## Verificación y límites

Resultados y capturas del navegador en `.qa/`, excluidos por `.gitignore`. La comprobación local utiliza un servidor HTTP estático equivalente; no ejecuta la extensión Live Server. Safari/iPhone físico queda pendiente. La sintaxis de JavaScript se comprueba con `node --check`.

Una única etiqueta `noindex, nofollow`. SVG monocromáticos, etiquetas de navegación, foco visible, enlace de salto, cierre del menú con Escape y respeto de `prefers-reduced-motion`. Las apariciones son discretas y se desactivan con movimiento reducido. La navegación permanece disponible sin JavaScript. Fuentes de Google Fonts con alternativas de sistema.

### Resultado del rediseño, 30/10/2026

Chrome sin interfaz, servido por HTTP local: 375, 390, 768, 1440 y 1920 px. En todos los anchos: sin desbordamiento horizontal, dos imágenes cargadas, cero anclas internas inexistentes, una única etiqueta robots `noindex, nofollow` y dos enlaces Booking con la URL canónica. En 375 y 390 px: apertura del menú, cierre al pulsar un enlace y cierre con Escape comprobados. Capturas de escritorio (1440) y móvil (375) inspeccionadas visualmente. Sintaxis JavaScript correcta. Estas pruebas no comprueban disponibilidad ni reservas en el sitio externo de Booking.

## Actualización con fotografías reales

Inspeccionados todos los archivos de `imgs/`: seis JPG y el JSON de metadatos. Las cuatro imágenes aportadas por el usuario son horizontales:

| Archivo original | Resolución | Contenido observado | Uso |
| --- | --- | --- | --- |
| 451565093.jpg | 1024 × 683 | Terraza con mesa, asientos, toldo y colinas al fondo | Hero |
| 451621257.jpg | 1024 × 575 | Dormitorio con cama y ventana | Galería |
| 451621278.jpg | 1024 × 478 | Salón, mesa de comedor y zona de cocina | Imagen grande de galería |
| 451621289.jpg | 1024 × 478 | Vistas desde la terraza a tejados y colinas | Galería |

Los originales se conservan intactos. Peso total de las cuatro fotografías: 376.017 bytes (aproximadamente 367 KiB); no se recomprimen ni se convierten a WebP por su peso ya reducido y para evitar otra generación de compresión. No se amplía artificialmente su resolución. Imágenes con dimensiones explícitas, proporciones originales, encuadres individuales centrados y sin recortes; lazy loading y decodificación asíncrona en la galería. Hero prioritario. La galería es estática, sin controles táctiles que dificulten el desplazamiento.

La portada pasa a foto completa y bloque de texto lateral en escritorio, foto y texto apilados en móvil, conservando paleta, tipografías, navegación, animaciones y pie. Las nuevas descripciones solo nombran lo observable; no confirman capacidades, servicios, condiciones ni uso de los equipos visibles. El río se mantiene identificado como entorno. Ninguna imagen de otro alojamiento representa la propiedad.

Verificación tras incorporar las fotos: Chrome por HTTP local a 375, 390, 768, 1440 y 1920 px. Las cinco imágenes visibles cargan, incluidas las de carga diferida; sin desbordamiento horizontal; anclas existentes; menú móvil abre y cierra mediante enlace y Escape; una única etiqueta noindex. Capturas de 375, 768 y 1440 px inspeccionadas visualmente para revisar proporciones y encuadres. No se ha probado Safari en iPhone real. Solo se han modificado archivos de este proyecto; sin commits, pushes ni despliegues.

## Repositorio

Version incorporada al repositorio GitHub por peticion expresa del usuario: https://github.com/pabloldl/laterracitadelbosque . Se mantiene noindex, nofollow; .qa/ queda excluido. Las menciones anteriores a ausencia de commits describen las fases locales previas. Esta subida no incluye despliegue.
