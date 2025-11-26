## 📋 Resumen del Rol

Como **Frontend Developer Semi-Senior**, el objetivo principal fue traducir los diseños de UI/UX en una interfaz web funcional, performante y accesible. El rol implicó no solo la maquetación, sino también la gestión del estado de la aplicación, la integración con APIs y la optimización de la experiencia de compra del usuario.

---

## 🚀 Responsabilidades Clave

### 1. Arquitectura y Configuración del Proyecto

* **Selección de Stack:** Participación en la decisión de tecnologías (ej. React/Next.js o Vue/Nuxt) basándose en los requisitos de SEO y performance.
* **Estructura de Carpetas:** Definición de una estructura escalable para componentes, hooks, servicios y utilidades.
* **Configuración del Entorno:** Setup de linters (ESLint, Prettier), husky pre-commit hooks y variables de entorno para desarrollo/producción.

### 2. Desarrollo de Componentes (Component Library)

Creación de un sistema de diseño atómico reutilizable y consistente con la identidad visual de la marca de cremas (estética limpia, minimalista y confiable).

* **UI Kit:** Botones, inputs, tarjetas de producto, modales y alertas.
* **Cards de Producto:** Desarrollo de tarjetas interactivas con variantes (vista rápida, añadir al carrito, "out of stock").
* **Filtros Avanzados:** Lógica para filtrar por tipo de piel, ingredientes y rango de precio.

### 3. Gestión del Estado (State Management)

Manejo de la lógica de negocio en el cliente para asegurar una navegación fluida.

* **Carrito de Compras:** Persistencia del carrito (LocalStorage/SessionStorage) y sincronización en tiempo real.
* **Autenticación:** Gestión de tokens (JWT), rutas protegidas (Perfil, Checkout) y manejo de sesiones de usuario.
* **Contexto Global:** Uso de Context API o Redux/Zustand para manejar temas y preferencias del usuario.

### 4. Integración con Backend (API Consumption)

Conexión con los endpoints del servidor para dinámizar la data.

* **Fetching de Datos:** Implementación de `Axios` o `Fetch API` con manejo robusto de errores y estados de carga (Loading Skeletons).
* **Optimización:** Uso de estrategias como `SWR` o `React Query` para caché y revalidación de datos.
* **Checkout Flow:** Integración segura con pasarelas de pago (ej. Stripe, WebPay, MercadoPago).

### 5. Performance y SEO (Core Web Vitals)

Dado que es un e-commerce, la velocidad y la indexación son críticas.

* **Lazy Loading:** Carga diferida de imágenes de alta calidad de los productos para no bloquear el renderizado inicial.
* **Code Splitting:** División del código para cargar solo el JS necesario por página.
* **Metadatos:** Implementación dinámica de etiquetas `<meta>` para cada producto (Open Graph, Title, Description).

---

## 🛠️ Stack Tecnológico


| Categoría               | Tecnologías                                          |
| :------------------------- | :------------------------------------------------------ |
| **Core**                 | HTML5, CSS3, JavaScript (ES6+) / TypeScript           |
| **Framework**            | React.js / Vue.js / Next.js (según aplique)          |
| **Estilos**              | CSS Modules / Tailwind CSS / SASS / Styled Components |
| **Estado**               | Redux Toolkit / Zustand / Context API                 |
| **API**                  | Axios, RESTful APIs                                   |
| **Control de Versiones** | Git, GitHub/GitLab                                    |
| **Paquetería**          | NPM / Yarn                                            |

---

## 🎨 Desafíos Específicos del Nicho (Cosmética)

En este proyecto, se prestó especial atención a detalles visuales que transmiten "limpieza" y "calidad":

* **Micro-interacciones:** Animaciones suaves al añadir cremas al carrito (feedback visual positivo).
* **Galería de Imágenes:** Implementación de zoom de alta resolución para ver texturas de las cremas y envases.
* **Accesibilidad (a11y):** Asegurar contraste de colores adecuado y navegación por teclado, cumpliendo estándares WCAG.

---

## 🔄 Flujo de Trabajo (Workflow)

1. **Daily Standups:** Reuniones diarias para sincronización con el equipo de Backend y Diseño.
2. **Code Review:** Revisión de Pull Requests de desarrolladores Junior, asegurando calidad de código y buenas prácticas.
3. **QA Testing:** Pruebas unitarias (Jest/Vitest) en componentes críticos y pruebas E2E (Cypress) para el flujo de compra.
4. **Despliegue (CI/CD):** Configuración de pipelines para despliegues automáticos en Vercel/Netlify o AWS.

---


*Este proyecto fue desarrollado siguiendo metodologías ágiles (Scrum/Kanban).*
