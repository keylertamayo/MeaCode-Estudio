# Optimizaciones de compilación

Este documento resume las optimizaciones vigentes de build y rendimiento de desarrollo.

## Rust / Cargo

### Perfil de desarrollo
- `opt-level = 1` para el código del workspace.
- `opt-level = 3` para dependencias.
- `incremental = true`.

### Perfil release
- `opt-level = 3`.
- `lto = true`.
- `codegen-units = 1`.
- `panic = "abort"`.

## Frontend (Vite)

- Preoptimización de dependencias pesadas.
- División de chunks para mejorar caché.
- Separación de bundles principales (React, Monaco, Terminal).

## Comandos útiles

```bash
# Desarrollo
pnpm tauri:dev

# Build de producción
pnpm tauri:build

# Limpiar artefactos Rust
cargo clean
```

## Observaciones

- La primera compilación siempre tarda más por descarga y compilación inicial de dependencias.
- Las compilaciones siguientes aprovechan caché incremental.

