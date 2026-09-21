# Regla de Control de Versiones y Sincronización para index.html

Cada vez que el asistente vaya a trabajar o modificar el archivo index.html en este proyecto:

1. **Sincronización Previa (Descargar cambios remotos de forma automática)**:
   - Antes de modificar cualquier archivo, ejecutar `git pull origin main` (o `git pull --rebase origin main`) para asegurar que se trabaja sobre la última versión subida a GitHub por otros colaboradores.

2. **Commit de versión nueva (Guardar respaldo local)**:
   - Inmediatamente después de realizar modificaciones en `index.html`, crear un commit en Git con un mensaje claro y descriptivo (ej: `Actualizar index.html: [descripción de los cambios]`).
   - Crear un tag de versión si aplica (ej: `v1.0.1`).

3. **Publicación (Subir a GitHub)**:
   - Ejecutar `git push origin main --tags` para publicar la nueva versión en GitHub.

4. **Garantía de respaldo y rollback**:
   - Para recuperar una versión anterior si surge un error:
     `git restore --source=HEAD~1 index.html`
