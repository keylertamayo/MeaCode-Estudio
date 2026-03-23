# Cómo contribuir a MeaCode Studio

Gracias por tu interés en contribuir. Este documento define reglas prácticas para colaborar de forma ordenada.

## Código de conducta

Al participar en el proyecto, aceptas mantener un trato respetuoso y profesional.

## Formas de contribuir

### Reporte de issues
- Usa el tracker de GitHub para bugs o propuestas.
- Incluye pasos para reproducir, comportamiento esperado y real.
- Revisa issues existentes antes de crear uno nuevo.

### Pull requests
1. Haz fork del repositorio y crea rama desde `main`.
2. Implementa cambios siguiendo estándares del proyecto.
3. Prueba tus cambios.
4. Abre PR con descripción clara del alcance e impacto.

## Requisitos de entorno

- Node.js 18 o superior.
- pnpm 9 o superior.
- Rust estable.
- Git.

## Configuración inicial

```bash
git clone https://github.com/TU_USUARIO/MeaCode-Studio.git
cd MeaCode-Studio
pnpm install
pnpm tauri dev
```

## Estándares de código

### Rust
- Seguir guías de API de Rust.
- Formatear con `cargo fmt`.
- Revisar con `cargo clippy`.
- Agregar pruebas cuando corresponda.

### TypeScript/React
- Usar TypeScript en nuevo código.
- Preferir componentes funcionales y hooks.
- Mantener nombres claros y consistentes.
- Formatear con Prettier.

### Commits
- Mensajes claros y en presente.
- Referenciar issue cuando aplique.

Ejemplo:
```text
feat: agregar menú contextual del explorador
fix: corregir ajuste de tamaño de terminal
docs: actualizar guía de instalación
```

## Estrategia de ramas

- `main`: rama estable.
- `feature/*`: nuevas funcionalidades.
- `fix/*`: correcciones.
- `docs/*`: documentación.

## Pruebas

- Validar funcionalidad nueva y regresiones básicas.
- Ejecutar checks disponibles antes de abrir PR.
- Probar en la plataforma objetivo cuando sea posible.

## Control de alcance

Cambios grandes (refactors mayores, rediseño de arquitectura o breaking changes) deben discutirse antes de abrir PR.

## Propiedad intelectual

Al contribuir, aceptas que tu contribución puede ser utilizada, modificada y distribuida como parte de software propietario de MeaCore Enterprise, bajo la licencia del proyecto.

## Derechos de terceros

Al abrir un PR declaras que tienes derecho a compartir ese código y que no infringe licencias de terceros.

## Proceso de revisión

1. Todo PR requiere revisión antes de merge.
2. Se valida calidad de código, pruebas y alineación con objetivos.
3. Atiende feedback de forma clara y oportuna.
4. El tiempo de revisión depende de la complejidad.

## Soporte

Si tienes dudas:
- Abre una discusión en GitHub.
- Revisa documentación existente.
- Consulta issues/PRs cerrados relacionados.

