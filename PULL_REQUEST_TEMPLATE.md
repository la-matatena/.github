## Descripción del cambio
<!-- Resume brevemente qué problema resuelve este Pull Request o qué nueva funcionalidad introduce. -->

## Tipo de cambio
- [ ] `feat`: Nueva funcionalidad
- [ ] `fix`: Corrección de error o bug
- [ ] `docs`: Modificación o añadido en la documentación
- [ ] `refactor`: Reorganización o mejora de código sin cambiar funcionalidad externa
- [ ] `test`: Incorporación o mejora de pruebas unitarias
- [ ] `chore`: Tareas de compilación, empaquetado o dependencias

## Incidencias relacionadas
<!-- Ej: Closes #123 / Fixes #456 -->
Closes #

## Lista de verificación de estándares La Matatena (MTTN Standards)
- [ ] El código cumple con las directrices de [CONVENTIONS.md](https://github.com/la-matatena/.github/blob/main/CONVENTIONS.md).
- [ ] Los identificadores y nombres respetan el prefijo `MTTN` y la paleta de color (`#8367c7` / `#6a4fb3`).
- [ ] Las pruebas unitarias pasan limpiamente en local (`make test` o `python3 -m unittest ...`).
- [ ] Se han actualizado las pruebas para cubrir la nueva lógica o corrección.
- [ ] La documentación (`README.md`, `docs/`) ha sido actualizada si el cambio afecta al usuario.
- [ ] No se incluyen claves, credenciales o archivos temporales no deseados.

## Pruebas realizadas
<!-- Describe qué comandos o pruebas ejecutaste para verificar este cambio y cuál fue el resultado. -->
```bash
# Ejemplo:
python3 -m unittest discover -s . -p "*_test.py"
```
