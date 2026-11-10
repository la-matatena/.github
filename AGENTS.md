# Guía para agentes de IA (La Matatena)

Contexto compartido para asistentes de código (Antigravity, Gemini CLI, Claude Code, Codex, Cursor…) que trabajen en cualquier repositorio de [@la-matatena](https://github.com/la-matatena).

La fuente de verdad sobre nombres, marca, estructura y commits es [`CONVENTIONS.md`](CONVENTIONS.md). Este archivo solo resume lo que un agente necesita tener en cuenta.

## Reglas rápidas

- **Nombres**: producto `MTTN <PascalCase> [Sufijo]`, repo `mttn-<kebab-case>`, tags `vMAJOR.MINOR.PATCH`.
- **Commits**: Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`), en inglés.
- **Idioma**: documentación y textos de interfaz en español; código e identificadores en inglés.
- **Español primero**: respeta diacríticos (`á é í ó ú ü ñ`), `¿` `¡` y variantes regionales en cualquier procesamiento de texto o subtítulos.
- **Sin nube obligatoria**: todo debe funcionar offline. No añadas dependencias de APIs remotas sin preguntar.
- **Hardware de referencia**: iMac 2017 (Intel i5, 2 GB VRAM AMD Polaris) y Apple Silicon. Cuida la VRAM: el usuario suele tener DaVinci Resolve abierto a la vez.
- **DaVinci Resolve**: mantener compatibilidad con Free y Studio (Lua, plantillas Fusion, OpenFX).
- **Marca en UI**: morado `#8367c7` / `#6a4fb3` solo para acentos y acciones clave (ver tokens en `CONVENTIONS.md` §2).

## Cómo trabajar

- Cambios pequeños y enfocados; no reformatees archivos que no tocas.
- Varios archivos usan finales de línea CRLF: consérvalos al editar.
- Ejecuta los tests del repo (`tests/` o `*_test.py` / `*_test.cc`) antes de dar un cambio por terminado.
- Las capturas oficiales de `docs/images/` se generan a 1440×940.
- No publiques releases, tags ni hagas `push` sin confirmación explícita.
