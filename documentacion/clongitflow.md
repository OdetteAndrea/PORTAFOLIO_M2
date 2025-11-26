
# 📘 README – Guía de Clonación y Flujo de Trabajo

Bienvenido/a al repositorio del proyecto.

Este documento explica  **cómo clonar** , **cómo crear tu rama de trabajo** y **cómo contribuiremos usando un flujo de trabajo basado en GitFlow** para mantener el orden y la calidad del código.

---

## 🔽 1. Clonar el proyecto

1. Abre tu terminal.
2. Ejecuta:

```bash
git clone <URL-DE-ESTE-REPOSITORIO>
```

3. Entra al proyecto:

```bash
cd nombre-del-proyecto
```

4. Instala dependencias (si aplica):

```bash
npm install
```

---

## 🌿 2. Flujo de trabajo del equipo (GitFlow simplificado)

Trabajaremos con dos ramas principales:

* **main** → rama estable, solo recibirá cambios cuando tengamos la **versión 1.0** o releases importantes.
* **develop** → rama donde se integrará el trabajo de TODAS las personas del equipo.

Nadie debe hacer commits directos a `main`.

---

## 👤 3. Creación de ramas por colaborador

Cada integrante debe crear su propia rama siguiendo este formato:

```
gitflow/<cargo>/<nombre>
```

**Ejemplos válidos:**

* `gitflow/lider-tecnico/blandskron`
* `gitflow/frontend-junior/javiera`
* `gitflow/ux-designer/daniela`
* `gitflow/backend-senior/eric`

Esto permite mantener un orden claro por roles y responsables.

---

## 🛠️ 4. Pasos para crear tu rama

Asegúrate de estar en `develop`:

```bash
git checkout develop
git pull origin develop
```

Crea tu rama personal:

```bash
git checkout -b gitflow/<cargo>/<tu-nombre>
```

Ejemplo:

```bash
git checkout -b gitflow/backend-senior/blandskron
```

---

## 📤 5. Subir tus cambios al repositorio remoto

Después de hacer tus commits:

```bash
git add .
git commit -m "Descripción del cambio"
git push origin gitflow/<cargo>/<tu-nombre>
```

---

## 🔀 6. Integración a la rama develop

Cuando tengas avances listos:

1. Crea un **Pull Request** desde tu rama → hacia la rama  **develop** .
2. Un revisor aprobará y hará merge.
3. Continuarás trabajando normalmente en tu propia rama.

> ⚠️ **IMPORTANTE:**
>
> Nadie debe mergear directamente a `main`. Toda integración va a `develop`.

---

## 🚀 7. Lanzamiento de la versión 1.0

Cuando completamos la primera iteración del proyecto:

* Se hará un merge controlado `develop` → `main`.
* Esto marcará la  **Versión 1** .
* Después seguiremos iterando por versiones y sprints usando el mismo flujo.

---

## 🧩 8. Resumen visual del flujo

```
             ┌─────────────┐
             │    main      │  ← Solo versiones estables
             └──────▲───────┘
                    │ Release
             ┌──────┴───────┐
             │   develop     │  ← Integración del equipo
             └──────▲───────┘
                    │ Pull Request
     ┌───────────────────────────────────────────┐
     │   gitflow/<cargo>/<nombre>                │  ← Trabajo individual
     └───────────────────────────────────────────┘
```

---

## 🤝 9. Buenas prácticas

* Hacer commits pequeños y frecuentes.
* Escribir mensajes claros.
* Mantener tu rama actualizada con `develop`.
* Usar Pull Requests para mantener la calidad.
* Evitar mezclar tareas no relacionadas en un solo commit.
