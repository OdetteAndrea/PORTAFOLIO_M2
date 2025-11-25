# 🧪 Guía de QA Funcional y Revisión de Código

Este documento detalla el procedimiento estándar para realizar el aseguramiento de calidad (QA) en este proyecto web construido con **HTML5, CSS3, Bootstrap, JavaScript y jQuery**.

El objetivo es garantizar no solo que la interfaz funcione correctamente, sino que el código subyacente sea mantenible, performante y respete las buenas prácticas definidas por el equipo.

---

## 📋 Prerrequisitos

Antes de comenzar el QA, asegúrate de tener:

1.  El repositorio clonado en tu máquina local.
2.  La rama a probar (`feature/nombre-de-la-rama`) actualizada.
3.  Un navegador moderno (Chrome/Firefox/Edge) con las _DevTools_ habilitadas.
4.  Un editor de código (VS Code recomendado) para la revisión estática.

---

## 🚀 Fase 1: Pruebas Funcionales (Caja Negra)

En esta fase, probamos la aplicación desde la perspectiva del usuario final.

### 1. Responsividad y Grilla de Bootstrap

- **Acción:** Redimensionar el navegador a diferentes puntos de quiebre (Mobile `xs`, Tablet `md`, Desktop `lg`).
- **Criterio de Aceptación:**
  - Los elementos no deben superponerse ni desbordarse (scroll horizontal no deseado).
  - El menú de navegación debe colapsar correctamente en móviles (clase `.navbar-collapse`).
  - Las columnas deben apilarse o alinearse según las clases `col-*` definidas.

### 2. Interacciones de Usuario (jQuery)

- **Acción:** Probar todos los botones, formularios y modales.
- **Criterio de Aceptación:**
  - Los eventos `click`, `hover` y `submit` responden sin _lag_.
  - No hay errores en la consola del navegador (F12 > Console) al interactuar.
  - Las validaciones de formularios impiden el envío de datos vacíos o incorrectos.

### 3. Estilos Visuales (CSS)

- **Acción:** Verificar la consistencia visual.
- **Criterio de Aceptación:**
  - Los colores y tipografías coinciden con el diseño en Figma/Adobe XD.
  - Los estados `:hover` y `:focus` están presentes en todos los elementos interactivos para accesibilidad.

---

## 🔍 Fase 2: Revisión de Código (Caja Blanca)

**IMPORTANTE:** El QA debe auditar el código fuente para asegurar la calidad técnica. Revisa los siguientes 3 puntos críticos en el código:

### 1. Uso Eficiente de Selectores jQuery

> **Objetivo:** Evitar problemas de rendimiento por recorridos excesivos del DOM.

- **Qué buscar:**
  - Evitar selectores universales o muy genéricos dentro de bucles.
  - Asegurar que los selectores se guardan en variables si se usan más de una vez (Cacheo del DOM).
- **❌ Mal:** `$('.btn-guardar').click(...)` (si se usa repetidamente sin cachear).
- **✅ Bien:**
  ```javascript
  const $btnGuardar = $('#btnGuardar');
  $btnGuardar.on('click', function() { ... });
  ```

### 2. Estructura y Sobrescritura de Bootstrap

> **Objetivo:** Mantener la integridad del framework y evitar el "CSS Spaghetti".

- **Qué buscar:**
  - Revisar el archivo `styles.css` o `main.css`.
  - No se debe usar `!important` para sobrescribir estilos de Bootstrap a menos que sea estrictamente necesario (casos de utilidad).
  - Verificar que se usen las clases nativas de Bootstrap (ej. `mt-5`, `text-center`) en lugar de crear nuevas clases CSS para lo mismo.
- **Ejemplo de Revisión:** Si ves `.mi-margen { margin-top: 3rem; }`, sugiere cambiarlo por la clase nativa `mt-5` en el HTML.

### 3. Separación de Intereses (HTML vs JS)

> **Objetivo:** Código limpio y fácil de mantener.

- **Qué buscar:**
  - No debe haber JavaScript en línea (inline) dentro de las etiquetas HTML.
  - Los _event listeners_ deben estar en el archivo `.js` externo, no en atributos `onclick="..."`.
- **❌ Mal:** `<button onclick="guardarDatos()">Guardar</button>`
- **✅ Bien:**
  - HTML: `<button id="btnGuardar">Guardar</button>`
  - JS: `$('#btnGuardar').on('click', guardarDatos);`

---

## 🐞 Reporte de Bugs

Si encuentras una incidencia, crea un _ticket_ en Jira/Trello con el siguiente formato:

1.  **Título:** Breve descripción del error.
2.  **Pasos para reproducir:** Lista numerada exacta.
3.  **Comportamiento esperado:** Qué debería pasar.
4.  **Comportamiento actual:** Qué está pasando realmente.
5.  **Evidencia:** Capturas de pantalla o logs de la consola.
6.  **Gravedad:** Baja / Media / Alta / Bloqueante.

---

## ✅ Aprobación

Para aprobar el _Pull Request_, el QA debe comentar:

> "QA Funcional OK. Revisión de código: Aprobada (selectores optimizados y sin estilos inline)."
