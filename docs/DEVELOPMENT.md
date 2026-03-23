# Guía de desarrollo

Esta guía explica cómo preparar y desarrollar MeaCode Studio.

## Requisitos previos

### Software requerido
- Node.js 18 o superior.
- pnpm 9 o superior (según `packageManager`).
- Rust estable (1.70+).
- Git.

### Requisitos por sistema operativo

#### Windows
- Microsoft Visual C++ Build Tools.
- Windows SDK.

#### macOS
- Xcode Command Line Tools:
  ```bash
  xcode-select --install
  ```

#### Linux (Ubuntu/Debian)
```bash
sudo apt-get update
sudo apt-get install -y \
  libwebkit2gtk-4.1-dev \
  libappindicator3-dev \
  librsvg2-dev \
  libsoup2.4-dev \
  pkg-config \
  patchelf
```

## Configuración inicial

```bash
git clone https://github.com/MeaCore-Enterprise/MeaCode-Studio.git
cd MeaCode-Studio
pnpm install
```

## Flujo de desarrollo

### Ejecutar en modo desarrollo
```bash
pnpm tauri:dev
```

Esto inicia Vite y la app Tauri con recarga en caliente.

### Build de producción
```bash
pnpm tauri:build
```

## Calidad de código

### Formato frontend
```bash
pnpm format
pnpm format:check
```

### Chequeo de tipos
```bash
pnpm type-check
```

### Rust
```bash
cargo fmt
cargo clippy
```

## Estructura del proyecto

```text
MeaCode-Estudio/
├── kernel/
│   ├── kernel-core/
│   ├── kernel-lsp/
│   └── kernel-ai/
├── src/
│   ├── components/
│   ├── editor/
│   ├── panels/
│   ├── layout/
│   ├── hooks/
│   ├── utils/
│   └── ipc/
├── src-tauri/
│   ├── src/
│   ├── icons/
│   └── tauri.conf.json
└── docs/
```

## Configuración del actualizador

1. Generar claves:
   ```bash
   cd src-tauri
   pnpm tauri signer generate
   ```
2. Reemplazar `pubkey` en `src-tauri/tauri.conf.json`.
3. Configurar secretos:
   - `TAURI_SIGNING_PRIVATE_KEY`
   - `TAURI_SIGNING_PRIVATE_KEY_PASSWORD`

Nunca subas clave privada o contraseña al repositorio.

## Depuración

- Frontend: consola/DevTools.
- Backend Rust: logs por terminal.
- IPC Tauri: revisar errores en consola y handlers en `src-tauri/src/main.rs`.

## Pruebas

```bash
cargo test
pnpm test
```

## Problemas comunes

- Error de compilación Rust:
  ```bash
  rustup update
  cargo clean && pnpm tauri build
  ```
- Puerto ocupado en dev: liberar puerto o cambiar configuración de Vite.
- Comandos Tauri no responden: validar `tauri.conf.json`, registro de comandos y features en `Cargo.toml`.

## Recursos

- [Documentación Tauri](https://tauri.app/v1/guides/)
- [Documentación React](https://react.dev/)
- [Documentación Rust](https://doc.rust-lang.org/)
- [Monaco Editor](https://microsoft.github.io/monaco-editor/)
- [Documentación TypeScript](https://www.typescriptlang.org/docs/)

