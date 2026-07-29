# ATHENEA STUDIO — WEB

Tienda de moda online con diseño atemporal, carrito de compras, favoritos, login con Google y pagos reales — hecha en un solo archivo HTML, sin backend.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

## Vista previa

> Proyecto de desarrollo web personal — tienda de moda femenina hecha en Medellín, Colombia.

<!--
Agrega aquí tus capturas de pantalla. Crea una carpeta `screenshots/` junto a Athenea.html
y guarda ahí las imágenes con estos nombres (o cambia las rutas de abajo si usas otros):
-->

| | |
|---|---|
| ![Hero](screenshots/hero.png) | ![Colección](screenshots/coleccion.png) |
| ![Carrito y pago](screenshots/checkout.png) | ![Panel admin](screenshots/admin.png) |

## Tecnologías

- HTML5, CSS3, JavaScript Vanilla — sin frameworks, sin build step
- Firebase Authentication (login real con Google)
- Wompi Web Checkout (pagos reales: tarjeta, PSE, Nequi)
- EmailJS (confirmaciones de pedido y avisos de pago por correo)
- FontAwesome 6.4 para iconos
- Google Fonts (Cormorant Garamond, Inter, Montserrat)
- LocalStorage como base de datos (carrito, favoritos, pedidos, usuarios)

## Funcionalidades

- Catálogo de 8 productos con precios en pesos colombianos (COP)
- Filtros por categoría, precio y orden, y búsqueda en tiempo real
- Carrito de compras y lista de favoritos con persistencia (localStorage)
- Cálculo de envío según ciudad colombiana (gratis en Medellín, tarifas para otras ciudades)
- Login con Google (Firebase Auth) o correo/contraseña
- Checkout con pago real vía Wompi (tarjeta, PSE, Nequi) o transferencia manual (Bancolombia / Nequi) como respaldo
- Seguimiento de pedidos y panel de administración (estadísticas, pedidos, usuarios)
- Notificaciones automáticas por correo (EmailJS) y botón flotante de WhatsApp
- Modal de detalle de producto con selector de talla y color
- Diseño responsive, animaciones de scroll y accesibilidad cuidada (contraste AA, `prefers-reduced-motion`)

## Cómo usar

1. Descarga o clona el repositorio
2. Abre `Athenea.html` en cualquier navegador moderno
3. No requiere instalación ni servidor

## Configuración (para activar login y pagos reales)

El sitio funciona en **modo demo** sin ninguna configuración adicional. Para activar las integraciones reales, edita estas constantes dentro de `Athenea.html`:

| Constante | Qué activa | Dónde conseguirla |
|---|---|---|
| `FIREBASE_CONFIG` | Login real con Google | [console.firebase.google.com](https://console.firebase.google.com) → Authentication → habilitar proveedor Google |
| `WOMPI_CONFIG` | Pagos reales (tarjeta / PSE / Nequi) | [comercios.wompi.co](https://comercios.wompi.co) → Configuración → Llaves API |
| `EMAILJS_*` | Correos automáticos de pedido y pago | [dashboard.emailjs.com](https://dashboard.emailjs.com) |
| `BANK_INFO` | Datos de transferencia manual (respaldo) | Tus datos bancarios reales |

Mientras una constante empiece con `TU_`, esa integración queda desactivada y el sitio sigue funcionando con su alternativa local.

## Estructura del proyecto

```
ATHENEA WEB GABY/
├── Athenea.html      # Sitio completo: HTML + CSS + JS en un solo archivo
├── screenshots/       # Capturas para este README (opcional)
└── README.md
```

## Roadmap

- [ ] Backend real (Firestore) para que los pedidos y el catálogo no dependan del navegador de cada visitante
- [ ] Panel de administración para añadir/editar productos sin tocar código
- [ ] Autenticación de administrador ligada a la cuenta de Google en vez de una contraseña local
- [ ] Hospedar las imágenes propias en vez de depender de un CDN externo

## Autor

**Daniel Buitrrago** — Ingeniería de Sistemas, UNIMINUTO
