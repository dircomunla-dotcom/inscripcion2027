# Reglas de Proyecto y Control de Versiones

## Control de Versiones para `index.html`

- **Cada modificación a `index.html` debe registrarse como un nuevo commit en Git** para asegurar que no se pierda ninguna versión funcional y sea posible restaurar versiones anteriores si surge algún problema.
- Mensaje de commit estandarizado: `Actualizar index.html: [descripción de los cambios realizados]`.
- Después de commitear localmente, ejecutar `git push origin main --tags`.

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
