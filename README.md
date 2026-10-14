# 🌸 Papel & Purpurina - Papelería Creativa & Landing Page

Landing page completa, moderna y artesanal para un emprendimiento de papelería creativa que comercializa: **libretas, ficheros, stickers, libros para colorear y tarjetas de presentación**. Diseñada para transmitir calidez y buen gusto, permitiendo que los clientes exploren el catálogo y realicen consultas directas por WhatsApp con mensajes automáticos prediseñados.

---

## ✨ Características Principales

- **Código Limpio y Ultra Liviano:** Construido en un único archivo `index.html` con CSS y JavaScript nativo integrado (sin frameworks pesados).
- **Animaciones de Scroll Avanzadas:** Integración con **GSAP 3 + ScrollTrigger** para:
  - Armado y caída de elementos al cargar el Hero (libreta, stickers die-cut, lápiz artesanal).
  - Efecto de piezas que se pegan en un tablero con rebote elástico suave al entrar en pantalla.
  - Línea de tiempo animada con *scrub* en la sección "¿Cómo se arma tu pedido?".
  - Parallax suave en detalles decorativos de fondo.
  - Barra de progreso de lectura en la parte superior.
  - Respeto estricto a `prefers-reduced-motion` para máxima accesibilidad.
- **Estética Artesanal & Scrapbook:**
  - Paleta de colores pastel en armonía con acento coral vibrante.
  - Textura suave de papel natural y renglones de cuaderno.
  - Cintas washi tape con extremos dentados (`clip-path`).
  - Efecto sticker troquelado die-cut con relieve y sombras multicapa.
  - Ilustraciones vectoriales SVG ricas y detalladas sin dependencias externas de imágenes pesadas.
  - Soporte automático de **modo claro y oscuro** (`prefers-color-scheme`).
- **Comercio Directo por WhatsApp:**
  - Cada tarjeta de producto incluye botón de consulta directa que pre-arma el mensaje con el nombre y precio del producto.
  - Formulario de contacto interactivo que valida y abre el chat de WhatsApp con el detalle del pedido.
  - Botón flotante de WhatsApp con indicador de mensaje y pulso suave.
- **Secciones Completas:**
  1. Header fijo con navegación suave y menú responsive hamburguesa.
  2. Hero con llamadas a la acción y escena ilustrada.
  3. 5 Categorías principales (Libretas, Ficheros, Stickers, Colorear, Tarjetas).
  4. Productos destacados con filtros interactivos por categoría.
  5. "¿Cómo se arma tu pedido?" con 4 pasos explicativos.
  6. Pedidos personalizados con galería tipo muro polaroid y washi tape.
  7. Testimonios de clientes en notas adhesivas pastel.
  8. Preguntas frecuentes en acordeón interactivo.
  9. Contacto con datos de ubicación, redes sociales y formulario.
  10. Footer con enlaces y créditos.

---

## 🛠️ Guía Rápida de Personalización

Todos los datos principales están organizados para que puedas cambiarlos en minutos:

### 1. Datos de Contacto y Marca (JavaScript)
Al final de `index.html`, dentro de la etiqueta `<script>`, encontrarás el objeto `CONFIG`:

```javascript
const CONFIG = {
  // ✏️ Nombre de tu emprendimiento
  brandName: "Papel & Purpurina",
  
  // ✏️ Número de WhatsApp internacional sin '+' ni guiones ni espacios
  // Ejemplo: 5491112345678 (Código país 54 + 9 móvil + código de área + número)
  whatsappNumber: "5491112345678",
  
  // ✏️ Usuario de Instagram (sin @)
  instagramUser: "papelypurpurina",
  
  // ✏️ Ubicación visible para tus clientes
  location: "Buenos Aires, Argentina (Envíos a todo el país)",
  
  // ✏️ Teléfono en formato legible
  phoneDisplay: "+54 9 11 1234-5678",
  
  // ✏️ Mensaje por defecto para el chat
  defaultWaMessage: "¡Hola! Vi su página de Papelería Creativa y quisiera hacer una consulta 🌸"
};
```

### 2. Colores y Tipografías (CSS en `:root`)
En la cabecera del archivo, dentro de `:root`, podés ajustar la paleta según los colores de tu marca:

```css
:root {
  --c-accent: #FF5A5F;        /* Color principal de botones y llamadas a la acción */
  --c-accent-hover: #E8454A;  /* Hover del botón */
  
  /* Pasteles */
  --c-pink: #FFD6E0;
  --c-mint: #C8F0DF;
  --c-lilac: #DCD3FF;
  --c-butter: #FFF0B8;
  --c-sky: #CFE8FF;

  /* Fondo y texto (Estilo Hoja de Agenda Crema Pastel) */
  --c-paper: #FAF4E8;         /* Fondo color crema marfil estilo hoja de agenda */
  --c-paper-dark: #F3EBD9;    /* Tono crema para secciones alternadas */
  --c-ink: #262135;           /* Tinta para textos principales */
}
```

### 3. Reemplazar Ilustraciones por Fotos Reales
Cada tarjeta de producto cuenta con un contenedor `.product-thumb`. Para reemplazar el SVG ilustrado por una foto de tu producto real, simplemente insertá una etiqueta `<img>`:

```html
<div class="product-thumb">
  <span class="badge badge--mint product-badge">Bestseller</span>
  <img src="ruta/a/tu/foto.jpg" alt="Cuaderno Botánico A5" style="width:100%; height:100%; object-fit:cover; border-radius:12px;">
</div>
```

---

## 🚀 Cómo Visualizarlo Localmente

Podés abrir directamente el archivo `index.html` en cualquier navegador web moderno, o iniciar un servidor local:

```bash
# Con Node.js
npx -y serve -p 3000

# Con Python
python -m http.server 3000
```

Luego visitá `http://localhost:3000` en tu navegador.

---

Desarrollado con dedicación y buen gusto para emprendimientos creativos. 💌
