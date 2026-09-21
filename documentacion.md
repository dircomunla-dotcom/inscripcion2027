# Documentación del Proyecto - Inscripción 2027

Este documento contiene la información técnica, la estructura del proyecto, la gestión del trabajo colaborativo y la guía de uso del sistema de control de versiones para `index.html`.

---

## 📌 Información del Repositorio

- **Repositorio Remoto:** [https://github.com/dircomunla-dotcom/inscripcion2027.git](https://github.com/dircomunla-dotcom/inscripcion2027.git)
- **Rama Principal:** `main`
- **Organización / Propietario:** `dircomunla-dotcom`

---

## 👥 Trabajo Colaborativo (Múltiples personas al mismo tiempo)

### ¿Qué pasa si dos personas trabajan simultáneamente en el mismo archivo?

1. **Si modifican partes/secciones distintas:** Git fusiona (merge) automáticamente los cambios de ambas personas sin que nadie pierda nada.
2. **Si modifican exactamente las mismas líneas:** Git detecta un **conflicto**, congela la fusión y marca las líneas en conflicto (`<<<<<<<` / `>>>>>>>`) para decidir qué versión mantener. **Nunca se sobreescribe ni se borra trabajo a ciegas**.

### ¿Cómo tener siempre la última versión online de forma automática?

En este proyecto se estableció una **regla de trabajo automática**:
- **Paso 1 (Automático antes de modificar):** El asistente ejecuta `git pull origin main` para traer a tu disco local cualquier cambio recién subido a GitHub por tus compañeros.
- **Paso 2 (Automático al terminar la modificación):** Se crea el commit respaldando la versión en el historial local.
- **Paso 3 (Automático al publicar):** Se ejecuta `git push origin main --tags` para subir tu nueva versión a GitHub.

---

## 📁 Archivos del Proyecto

- **`index.html`**: Página principal del sistema de inscripción.
- **`paso1.html`**: Formulario / Paso 1 del proceso de inscripción.
- **`paso2.html`**: Formulario / Paso 2 del proceso de inscripción.
- **`articulo7-extranjeros.html`**: Requisitos del Artículo 7 para aspirantes extranjeros.
- **`documentacion.md`**: Este documento de referencia y guía de uso.
- **`AGENTS.md`**: Directivas de trabajo para el asistente de desarrollo.
- **`.agents/rules/git_versioning.md`**: Regla de sincronización y versionado automático.

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

## 🚀 Comandos Manuales de Sincronización

- **Descargar la última versión desde GitHub:**
  ```bash
  git pull origin main
  ```
- **Subir cambios locales a GitHub:**
  ```bash
  git push origin main --tags
  ```
