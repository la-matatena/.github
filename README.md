# La Matatena · Configuración y Estándares de la Organización

Este repositorio (`la-matatena/.github`) define la configuración global, las plantillas de comunidad heredadas automáticamente y los estándares técnicos de todos los repositorios bajo la organización [**@la-matatena**](https://github.com/la-matatena).

---

## 📁 Contenido del repositorio

- [**`CONVENTIONS.md`**](CONVENTIONS.md): Guía normativa completa de nomenclatura `MTTN`, paleta de marca `#8367c7` / `#6a4fb3`, estructura de repositorios, guías de README, diseño de insignias (badges) y flujos de CI/CD.
- [**`AGENTS.md`**](AGENTS.md): Resumen de las convenciones para asistentes de código con IA (Antigravity, Gemini CLI, Claude Code, Codex, Cursor…) que trabajen en cualquier repositorio de la organización.
- [**`profile/README.md`**](profile/README.md): Página de inicio pública que se renderiza en el perfil de la organización (`https://github.com/la-matatena`).
- [**`CONTRIBUTING.md`**](CONTRIBUTING.md): Guía de contribución por defecto para todos los repositorios de la organización.
- [**`CODE_OF_CONDUCT.md`**](CODE_OF_CONDUCT.md): Código de conducta estándar (Contributor Covenant v2.1).
- [**`SECURITY.md`**](SECURITY.md): Política de reporte de vulnerabilidades y seguridad.
- [**`SUPPORT.md`**](SUPPORT.md): Recursos y canales de ayuda y soporte.
- [**`PULL_REQUEST_TEMPLATE.md`**](PULL_REQUEST_TEMPLATE.md): Plantilla estándar de Pull Requests.
- [**`.github/ISSUE_TEMPLATE/`**](.github/ISSUE_TEMPLATE): Formularios de incidencias (GitHub Issue Forms) para reportes de errores y propuestas de funcionalidades.
- [**`assets/`**](assets): Logotipo oficial en SVG (`matatena-icon.svg`) y tokens de paleta de marca (`brand-palette.json`).
- [**`LICENSE`**](LICENSE): Texto canónico de la licencia MIT de La Matatena.

---

## 🔄 Herencia automática en GitHub

GitHub utiliza este repositorio como base comunitaria ("Community Health Files"):

1. Cualquier repositorio de `@la-matatena` que no incluya su propio `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `SUPPORT.md`, o plantillas de Issue/PR, hereda automáticamente las versiones centralizadas en este repositorio.
2. Si un repositorio particular necesita reglas adicionales o específicas, puede sobreescribirlas incluyendo sus propios archivos locales.
3. `LICENSE`, `CONVENTIONS.md` y `AGENTS.md` **no** se heredan. GitHub no admite una licencia por defecto, por eso cada repositorio incluye su propio `LICENSE` (MIT) y un `AGENTS.md` local con contexto del proyecto, como indica la [estructura estándar de un repositorio](CONVENTIONS.md#4-estructura-estándar-de-un-repositorio).

---

## 📚 Enlaces rápidos

- [Organización en GitHub](https://github.com/la-matatena)
- [Sitio oficial La Matatena](https://la-matatena.com)
- [Estándares MTTN](CONVENTIONS.md)
