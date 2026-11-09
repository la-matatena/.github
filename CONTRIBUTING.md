# Guía de Contribución a La Matatena (Contributing Guide)

¡Gracias por tu interés en contribuir a los proyectos de código abierto de **La Matatena**! Toda aportación—desde corrección de código y optimizaciones de rendimiento hasta ampliaciones de glosarios de juegos de mesa o mejoras en la documentación—es bienvenida.

---

## 🧭 ¿Cómo empezar?

1. **Revisa las normas de la organización**:
   Familiarízate con nuestras directrices de nombres, estilo de código y paleta visual en [**CONVENTIONS.md**](CONVENTIONS.md).
2. **Revisa las incidencias abiertas**:
   Busca en la pestaña *Issues* del repositorio correspondiente antes de iniciar un trabajo significativo para evitar duplicación.
3. **Abre un Issue previo para cambios mayores**:
   Si deseas proponer una nueva funcionalidad de gran escala o una reestructuración de arquitectura, crea un *Feature Request* primero para discutir el diseño con los mantenedores.

---

## 🛠️ Flujo de desarrollo con Git

1. **Haz un Fork** del repositorio a tu cuenta personal de GitHub.
2. **Crea una rama descriptiva** partiendo de `main`:
   ```bash
   git checkout -b feat/soporte-formato-ass
   # o
   git checkout -b fix/vram-leak-openfx
   ```
3. **Escribe código limpio y probado**:
   - Asegúrate de que las pruebas unitarias existentes continúen pasando.
   - Si añades una nueva funcionalidad, incluye pruebas que verifiquen su comportamiento.
   - Mantén los comentarios y cadenas de documentación en el idioma principal del proyecto.
4. **Sigue la convención de commits**:
   Utilizamos [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat: ...` para nuevas funcionalidades.
   - `fix: ...` para corrección de fallos.
   - `docs: ...` para mejoras de documentación.
   - `refactor: ...` para cambios de estructura sin alteración de funcionalidad.
   - `test: ...` para añadir o actualizar pruebas.
   - `chore: ...` para tareas de mantenimiento.
5. **Envía tu Pull Request**:
   - Completa la lista de verificación incluida en la plantilla de PR.
   - Vincula el PR a la incidencia que resuelve (`Closes #12`).

---

## 🧪 Pruebas locales y Verificación

Antes de abrir tu Pull Request, ejecuta la suite de pruebas del proyecto:

- **Proyectos Python**:
  ```bash
  python3 -m unittest discover -s . -p "*_test.py"
  ```
- **Proyectos C++ / OpenFX**:
  ```bash
  make test  # o ctest / bazel test //...
  ```

---

## ⚖️ Código de Conducta

Al participar en este proyecto, te comprometes a respetar y promover un entorno respetuoso e inclusivo tal como se define en nuestro [Código de Conducta](CODE_OF_CONDUCT.md).

---

## 📄 Licencia de tus contribuciones

Al contribuir código a cualquier repositorio bajo La Matatena, aceptas que tus contribuciones se licencien bajo los términos de la licencia [MIT](LICENSE) del proyecto.
