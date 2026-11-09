# Normas y Convenciones de La Matatena (MTTN Standards)

Este documento recopila las directrices oficiales que deben seguir **todos los repositorios y herramientas** desarrollados bajo la organización [**@la-matatena**](https://github.com/la-matatena).

---

## 1. Convención de Nombres (Naming Convention)

Todos los proyectos abiertos de La Matatena siguen una estructura unificada en nombres de repositorio, nombres de producto y artefactos binarios.

### 1.1 Nombre de producto
- **Fórmula**: `MTTN` + `NombreEnPascalCase` + `[SufijoOpcional]`
- **Ejemplos**:
  - `MTTN AutoSubs Tool`
  - `MTTN PaperCraft Studio`
  - `MTTN RuleBook Assistant` (futuro)
  - `MTTN DiceRoll Engine` (futuro)
- **Regla**: El prefijo `MTTN` (mayúsculas) identifica inmediatamente las herramientas pertenecientes al ecosistema de La Matatena.

### 1.2 Slug del repositorio (GitHub Repository Name)
- **Fórmula**: `mttn-<nombre-en-kebab-case>` (todo en minúsculas, separado por guiones).
- **Ejemplos**:
  - `la-matatena/mttn-autosubs-tool`
  - `la-matatena/mttn-papercraft-studio`

### 1.3 Nombres de artefactos, binarios y plugins
- **Paquetes comprimidos y releases**: `MTTN_<Nombre>_<version>_<plataforma>.zip` o `mttn-<nombre>-v<version>.zip`.
- **Plugins DaVinci Resolve / Fusion**:
  - Plantillas de títulos: prefijo `AutoSubs_ES_` o `MTTN_` (ej. `MTTN_PaperCraft_Torn_Border.setting`).
  - Scripts Lua: `1 - MTTN <Accion>.lua` (ej. `1 - MTTN AutoSubs - Exportar Audio.lua`).
  - Plugins OpenFX: `MTTN PaperCraft Studio.ofx.bundle`.
- **Librerías Python**: paquetes en `snake_case` o prefijados con `mttn_`.

### 1.4 Versionado y etiquetas (Tags)
- Seguimos [Semantic Versioning 2.0.0](https://semver.org/) (`vMAJOR.MINOR.PATCH`):
  - `MAJOR`: Cambios incompatibles con la API o flujos previos.
  - `MINOR`: Nuevas funcionalidades retrocompatibles.
  - `PATCH`: Corrección de errores y optimizaciones menores.
- Los tags en Git siempre llevan el prefijo `v`: `v1.0.0`, `v1.2.0`, `v2.1.0`.

---

## 2. Identidad Visual y Paleta de Marca

La identidad gráfica de La Matatena se basa en una gama de morados y violetas cálidos combinados con una estética editorial de estudio oscuro (*dark studio surfaces*).

### 2.1 Colores principales

| Token | Valor Hex | Uso principal |
| :--- | :--- | :--- |
| `--mttn-purple` | `#8367c7` | Color insignia de marca, badges primarios, acentos activos, botones destacados |
| `--mttn-purple-deep` | `#6a4fb3` | Color secundario profundo, badges complementarios, estados *hover* |
| `--mttn-purple-deep-hover` | `#583da0` | Interacciones hover intensas y selecciones |
| `--mttn-purple-control` | `#9f85e3` | Bordes de controles activos, barras de scroll, foco de accesibilidad |
| `--mttn-purple-tint` | `#d5c7f7` | Textos claros sobre fondos púrpuras, contrastes sutiles |
| `--mttn-purple-soft` | `rgba(131, 103, 199, 0.18)` | Fondos de tarjetas seleccionadas, chips activos, realces |

### 2.2 Superficies oscuras (Dark Studio Surfaces)

| Token | Valor Hex | Uso |
| :--- | :--- | :--- |
| `--bg` | `#110f17` | Fondo principal de la ventana o aplicación |
| `--topbar-bg` | `#15121e` | Barra superior de navegación / cabecera |
| `--panel` | `#171421` | Columnas y contenedores de herramientas |
| `--card` | `#1d1929` | Tarjetas modulares de controles |
| `--surface-inset` | `#13101b` | Cajas de texto, pistas de progreso, fondos de onda |
| `--surface-elevated` | `#272138` | Menús desplegables, tooltips, modales |
| `--border` | `#342d4a` | Bordes sutiles entre paneles y tarjetas |
| `--border-control` | `#736599` | Bordes de botones e inputs interactivos |
| `--text` | `#f3effb` | Texto primario legible de alto contraste |
| `--muted` | `#b2aad0` | Textos secundarios, descripciones y pistas |

### 2.3 Tipografía
- **Títulos y cabeceras**: `"Montserrat", -apple-system, BlinkMacSystemFont, "SF Pro Display", "Helvetica Neue", sans-serif`.
- **Cuerpo de texto**: `-apple-system, BlinkMacSystemFont, "SF Pro Text", "Helvetica Neue", Arial, sans-serif`.
- **Código y códigos de tiempo (Timecode)**: `ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace`.

### 2.4 Logotipo de La Matatena
El icono vectorial oficial se encuentra en [`assets/matatena-icon.svg`](assets/matatena-icon.svg). Muestra la silueta geométrica de la matatena tradicional mexicana con bordes redondeados y fondo `#8367c7`.

---

## 3. Insignias de Repositorio (Badges Estándar)

Cada repositorio debe incluir en la cabecera de su `README.md` un bloque de insignias estándar generadas con [Shields.io](https://shields.io) empleando la paleta de marca:

```markdown
[![CI & Release](https://github.com/la-matatena/<repo>/actions/workflows/ci-release.yml/badge.svg)](https://github.com/la-matatena/<repo>/actions/workflows/ci-release.yml)
[![Latest Release](https://img.shields.io/github/v/release/la-matatena/<repo>?color=8367c7&label=release)](https://github.com/la-matatena/<repo>/releases/latest)
[![License: MIT](https://img.shields.io/badge/license-MIT-8367c7.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux-6a4fb3.svg)](docs/installation.md)
[![Brand: La Matatena](https://img.shields.io/badge/La%20Matatena-MTTN-8367c7.svg)](https://github.com/la-matatena)
```

---

## 4. Estructura Estándar de un Repositorio

Un repositorio bajo `@la-matatena` debe seguir esta organización mínima de archivos:

```text
mttn-<nombre>/
├── .github/
│   └── workflows/
│       └── ci-release.yml      # Integración continua, tests y empaquetado
├── docs/                       # Documentación técnica, guías de usuario y arquitectura
│   └── images/                 # Capturas oficiales de interfaz en 1440x940
├── tests/ (o *_test.py/.cc)    # Batería de pruebas unitarias automatizadas
├── LICENSE                     # Licencia MIT canónica
├── README.md                   # Descripción general, capturas, tablas de entregables y guía rápida
└── <código fuente del proyecto>
```

---

## 5. Requisitos del `README.md`

Todo `README.md` principal debe contar con las siguientes secciones:

1. **Título H1**: `# MTTN <Nombre> <Sufijo>`
2. **Badges**: bloque de badges con colores de marca (`8367c7` / `6a4fb3`).
3. **Párrafo de introducción**: Nombre en negrita, mención a **[La Matatena](https://la-matatena.com)** y cuenta `@la-matatena`, resumen de propósito y hardware objetivo.
4. **Callout de convención de marca**:
   ```markdown
   > **La Matatena Open Projects Convention:** All open tools under [`github.com/la-matatena`](https://github.com/la-matatena) follow the **`MTTN` + `TwoWordNameInPascalCase` + `[Suffix]`** naming standard (e.g., **MTTN AutoSubs Tool**, **MTTN PaperCraft Studio**) and La Matatena's `#8367c7` / `#6a4fb3` brand palette.
   ```
5. **Capturas de pantalla o diagramas** (`docs/images/`).
6. **Tabla de entregables / componentes incluidos**.
7. **Guía de instalación rápida paso a paso**.
8. **Licencia y créditos**: Licencia MIT con enlace al archivo `LICENSE`.

---

## 6. Filosofía de Desarrollo y Arquitectura

1. **Ejecución local y sin dependencias de nube obligatorias**:
   Las herramientas deben poder funcionar 100% desconectadas, protegiendo la privacidad del contenido audiovisual del creador.
2. **Especialización en español**:
   Considerar siempre diacríticos (`á, é, í, ó, ú, ü, ñ`), mayúsculas acentuadas, signos de apertura (`¿`, `¡`) y dialectos hispanohablantes (Neutro, España Peninsular, México/LatAm, Río de la Plata).
3. **Optimización de recursos (Memory & GPU Safety)**:
   Proteger la VRAM de la GPU cuando se trabaja conjuntamente con software pesado (DaVinci Resolve, Premiere, Blender). Ofrecer modos CPU multi-hilo (AVX2, NEON) seguros.
4. **Compatibilidad con DaVinci Resolve Free y Studio**:
   Siempre que sea posible, brindar compatibilidad tanto para la versión gratuita como para la versión Studio mediante puentes de scripts Lua, plantillas Fusion o plugins OpenFX universales.

---

## 7. Flujo de Git y Mensajes de Confirmación (Commits)

Utilizamos el estándar **Conventional Commits**:

- `feat:` Nuevas funcionalidades para el usuario.
- `fix:` Corrección de errores.
- `docs:` Cambios o ampliaciones exclusivamente en documentación.
- `chore:` Tareas de mantenimiento, actualización de dependencias, scripts de release.
- `refactor:` Reestructuración de código sin alterar su comportamiento externo.
- `test:` Añadido o corrección de pruebas unitarias.

**Ejemplo**:
```bash
git commit -m "feat: add BGG tabletop glossary support to subtitle pipeline"
git commit -m "fix: prevent memory leak in OpenFX texture upload"
```
