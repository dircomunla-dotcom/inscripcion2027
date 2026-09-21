# Regla de Control de Versiones para index.html

Cada vez que el asistente modifique el archivo index.html en este proyecto:

1. **Commit de versión nueva**:
   - Crear un commit en Git inmediatamente después de realizar la modificación.
   - Usar un mensaje claro y explicativo de los cambios (ej: `Actualizar index.html: [descripción breve del cambio]`).
   - Crear un tag incremental opcional si es un hito importante (ej: `v1.0.1`, `v1.0.2`).

2. **Push a remoto**:
   - Intentar hacer `git push origin main --tags`.
   - Si la autenticación remota requiere interacción del usuario, notificar al usuario que la versión local está guardada y lista para ser subida.

3. **Garantía de respaldo y rollback**:
   - Nunca sobrescribir la historia previa sin antes asegurar el commit.
   - En cualquier momento el usuario puede pedir volver a una versión anterior utilizando:
     `git restore --source=HEAD~1 index.html` (para volver a la versión inmediatamente anterior)
     o `git checkout <commit_hash_o_tag> index.html`.
