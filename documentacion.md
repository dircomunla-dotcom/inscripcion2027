# Documentación del Proyecto - Inscripción 2027

Este documento contiene la información técnica, la estructura del proyecto y la guía de uso del sistema de control de versiones y respaldos automáticos para el archivo `index.html`.

---

## 📌 Información del Repositorio

- **Repositorio Remoto:** [https://github.com/dircomunla-dotcom/inscripcion2027.git](https://github.com/dircomunla-dotcom/inscripcion2027.git)
- **Rama Principal:** `main`
- **Organización / Propietario:** `dircomunla-dotcom`

---

## 📁 Archivos del Proyecto

- **`index.html`**: Página principal del sistema de inscripción (gestionada con control de versiones estricto).
- **`paso1.html`**: Formulario / Paso 1 del proceso de inscripción.
- **`paso2.html`**: Formulario / Paso 2 del proceso de inscripción.
- **`articulo7-extranjeros.html`**: Sección / Requisitos del Artículo 7 para aspirantes extranjeros.
- **`AGENTS.md`**: Reglas y directivas de trabajo para el asistente de desarrollo.
- **`.agents/rules/git_versioning.md`**: Regla automática de control de versiones.

---

## 🛡️ Sistema de Control de Versiones y Respaldo para `index.html`

Cada vez que se trabaje en este proyecto y se modifique el archivo `index.html`, se genera de forma automática un **nuevo commit en Git** (y opcionalmente una etiqueta de versión como `v1.0.1`, `v1.0.2`, etc.).

Esto garantiza que **nunca se pierda una versión previa funcional** y sea posible volver atrás en cualquier momento si surge un fallo o error en la versión nueva.

---

## ⏪ Guía de Reversión y Restauración de Versiones

Si necesitas restaurar una versión anterior de `index.html`:

### 1. Volver a la versión inmediatamente anterior (1 paso atrás)
```bash
git restore --source=HEAD~1 index.html
```

### 2. Consultar el historial completo de versiones
```bash
git log --oneline index.html
```

### 3. Restaurar un commit o versión específica por su Hash o Tag
```bash
git restore --source=<HASH_O_TAG> index.html
```
*Ejemplo:*
```bash
git restore --source=v1.0.0 index.html
```

---

## 🚀 Comandos para Sincronizar con GitHub

Para enviar manualmente los commits y tags locales al repositorio remoto:
```bash
git push origin main --tags
```
