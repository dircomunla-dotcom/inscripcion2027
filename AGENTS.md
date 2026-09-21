# Reglas de Proyecto y Control de Versiones

## Flujo de Trabajo Automático para `index.html`

1. **Antes de editar:** Ejecutar siempre `git pull origin main` para descargar la versión más reciente alojada en GitHub.
2. **Después de editar:** Registrar los cambios inmediatamente en Git: `git commit -am "Actualizar index.html: [descripción]"`
3. **Publicar cambios:** Subir la nueva versión a GitHub: `git push origin main --tags`

## Manejo de Trabajo Concurrente (Múltiples personas)

- Si otra persona subió cambios a GitHub mientras trabajabas, `git pull` descargará e integrará automáticamente esos cambios.
- Si dos personas modificaron las mismas líneas exactamente, Git avisará de un **conflicto** para revisar y decidir qué versión conservar sin perder ningún cambio.

## Cómo Restaurar una Versión Anterior de `index.html`

Si en algún momento una nueva versión tiene un error y deseas restaurar la versión anterior:

1. **Volver a la versión inmediatamente anterior (1 paso atrás):**
   ```bash
   git restore --source=HEAD~1 index.html
   ```

2. **Ver el historial de todas las versiones guardadas:**
   ```bash
   git log --oneline index.html
   ```

3. **Restaurar un commit o versión específica por su Hash o Tag:**
   ```bash
   git restore --source=<HASH_O_TAG> index.html
   ```
