Basado en el documento "Estructura de la Página Web 'El Alma'", he diseñado una matriz de casos de prueba funcional. Dado que el stack es **HTML/CSS/Bootstrap/jQuery**, he incluido validaciones técnicas específicas para esas tecnologías.

Aquí tienes los casos de prueba organizados por sección:

### 1. Cabecera (Header) y Navegación

**Objetivo:** Verificar la funcionalidad del menú fijo y la navegación.

| ID       | Caso de Prueba               | Pasos / Acción                                          | Resultado Esperado                                                                                                                | Fuente |
| :------- | :--------------------------- | :------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------- | :----- |
| **H-01** | Comportamiento Sticky (Fijo) | Hacer scroll hacia abajo en la página (al menos 500px). | La barra de navegación debe permanecer visible y fija en la parte superior (`position: fixed` o clase `sticky-top` de Bootstrap). |
| **H-02** | Enlaces de Navegación        | Verificar los textos del menú central.                  | Deben existir exactamente 5 enlaces: "Inicio", "Rostro", "Cuerpo", "Envíos", "Promociones".                                       |
| **H-03** | Contador del Carrito         | Observar el icono del carrito a la derecha.             | Debe visualizarse un contador (badge) sobre el icono.                                                                             |

### 2. Sección Hero (Principal)

**Objetivo:** Validar la correcta visualización de la primera pantalla utilizando el sistema de grillas de Bootstrap.

| ID       | Caso de Prueba            | Pasos / Acción                                                | Resultado Esperado                                                                          | Fuente |
| :------- | :------------------------ | :------------------------------------------------------------ | :------------------------------------------------------------------------------------------ | :----- |
| **M-01** | Visualización Full Screen | Cargar la página en un monitor de escritorio.                 | La sección debe ocupar toda la pantalla inicial (100vh).                                    |
| **M-02** | Botones de Acción (CTA)   | Verificar la existencia de botones bajo el texto descriptivo. | Deben existir dos botones funcionales: "Descubrir la Colección" y "Conocer Más".            |
| **M-03** | Estilos Tipográficos      | Inspeccionar el título "Conexión con la naturaleza...".       | La fuente debe ser **Cormorant Garamond** (Serif elegante) y color Marrón oscuro (#3D3D3D). |

### 3. Productos Destacados (Interacciones jQuery)

**Objetivo:** Probar la interacción dinámica de las tarjetas de producto.

| ID       | Caso de Prueba          | Pasos / Acción                                                     | Resultado Esperado                                                                            | Fuente |
| :------- | :---------------------- | :----------------------------------------------------------------- | :-------------------------------------------------------------------------------------------- | :----- |
| **P-01** | Renderizado de Tarjetas | Contar las tarjetas visibles en la sección "Productos Destacados". | Deben mostrarse 3 tarjetas alineadas horizontalmente (probablemente `col-md-4` en Bootstrap). |
| **P-02** | Efecto Zoom (Hover)     | Pasar el cursor del mouse sobre la imagen de cualquier producto.   | La imagen debe tener un efecto de zoom suave (transformación CSS o animación jQuery).         |
| **P-03** | Datos del Producto      | Verificar el contenido de una tarjeta (ej. Crema Hidratante).      | Debe mostrar: Etiqueta de categoría, Nombre, Precio ($24.990) y botón "Agregar".              |

### 4. Envíos y Promociones

**Objetivo:** Verificar la información estática y la disposición de elementos.

| ID        | Caso de Prueba        | Pasos / Acción                                       | Resultado Esperado                                                                        | Fuente |
| :-------- | :-------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------------------------- | :----- |
| **E-01**  | Iconos de Beneficios  | Revisar la sección de "Envíos a Regiones".           | Deben aparecer 4 iconos: Envío nacional, Retiro en tienda, Entrega rápida, Envío seguro.  |
| **PR-01** | Tarjetas de Promoción | Verificar las ofertas listadas.                      | Deben existir bloques para: 20% Descuento, Kit de Regalo, 2x1 Mascarillas y Club El Alma. |
| **PR-02** | Código de Descuento   | Leer el detalle de la tarjeta de "20% de Descuento". | Debe ser legible el código "BIENVENIDA20".                                                |

### 5. Pie de Página (Footer) y Formularios

**Objetivo:** Validar enlaces y estructura de cierre.

| ID       | Caso de Prueba        | Pasos / Acción                                                                | Resultado Esperado                                                                      | Fuente |
| :------- | :-------------------- | :---------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :----- |
| **F-01** | Columnas del Footer   | Inspeccionar la estructura del pie de página.                                 | Debe haber 4 columnas organizadas: Marca, Productos, Ayuda y Contacto (Grid Bootstrap). |
| **F-02** | Formulario Newsletter | Ubicar el campo de suscripción (generalmente cerca del footer o promociones). | Debe existir un campo de entrada para email y un botón de suscripción funcional.        |

### 6. Botón de Ayuda Flotante (Lógica JS Crítica)

**Objetivo:** Esta es la funcionalidad más compleja en cuanto a JavaScript/jQuery del sitio.

| ID       | Caso de Prueba            | Pasos / Acción                             | Resultado Esperado                                                                                        | Fuente |
| :------- | :------------------------ | :----------------------------------------- | :-------------------------------------------------------------------------------------------------------- | :----- |
| **A-01** | Posicionamiento Fijo      | Hacer scroll a lo largo de toda la página. | El círculo verde debe permanecer fijo en la esquina inferior derecha en todo momento.                     |
| **A-02** | Interacción de Despliegue | Hacer clic en el botón flotante.           | Se deben desplegar 3 opciones ocultas: WhatsApp, Teléfono y Email (Toggle class o `slideDown` de jQuery). |

### 🧪 Sugerencia Técnica para el QA

Probar la **responsividad** reduciendo el ancho del navegador a tamaño móvil (menos de 576px).

- **Prueba extra:** Verificar que las 3 tarjetas de productos y las 4 columnas del footer se apilen verticalmente (colapsen) en vista móvil para no romper el diseño.
