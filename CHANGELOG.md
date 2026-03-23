# Historial de cambios

Todos los cambios relevantes del proyecto se documentan aquí.

Formato basado en [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) y versionado semántico ([SemVer](https://semver.org/spec/v2.0.0.html)).

## [Unreleased]

### Planificado
- Estabilización del acceso a sistema de archivos.
- Mejora de persistencia de configuración.
- Mejoras de UX en el actualizador automático.

## [0.1.0]

### Añadido
- Editor inicial con integración de Monaco Editor.
- Terminal integrada con xterm.
- Paleta de comandos (`Ctrl+Shift+P`).
- Navegación rápida de archivos (`Ctrl+P`).
- Panel de chat IA con integración Nexusify API.
- Panel explorador de archivos.
- Editor por pestañas con soporte multiarchivo.
- Menú contextual con acciones de código asistidas por IA.
- Persistencia de sesión.
- Panel Run/Debug.
- UI moderna con Tailwind CSS.
- Layout adaptable.

### Técnico
- Integración de framework de escritorio Tauri.
- Frontend con React + TypeScript.
- Backend en Rust con arquitectura por kernel.
- Base de servidor LSP (`kernel-lsp`).
- Base de motor IA (`kernel-ai`).
- Implementación base del núcleo (`kernel-core`).

---

Nota: no eliminar la sección `[Unreleased]`. Al publicar una versión, mover ítems desde `[Unreleased]` al bloque de versión correspondiente.

