# Workflows — theme-toolkit

> Authoritative runbooks and dev workflows for `theme-toolkit`.

---

## 1. Adding a New Platform Packager Target

1. Implement packager module in `src-tauri/src/packager/<platform>.rs`.
2. Implement the `ThemePackager` trait (`validate_assets`, `package`, `apply`).
3. Add command in `src-tauri/src/commands.rs` and register in `src-tauri/src/lib.rs`.
4. Add frontend export action in `src/lib/components/export/`.
5. Run full verification: `npm run check` and `RUSTFLAGS="-D warnings" cargo test`.

---

## 2. Adding a New Theme Token or Asset Type

1. Update theme schema definition in `src-tauri/src/theme/schema.rs`.
2. Update TypeScript interface in `src/lib/types/theme.ts`.
3. Add SCSS design token in `src/lib/styles/tokens.scss`.
4. Update preview components in `src/lib/components/preview/`.
