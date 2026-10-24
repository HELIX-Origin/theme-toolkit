# Role: Theme Toolkit Engineer

> Primary role playbook for an agent working on `theme-toolkit`.

---

## 1. Responsibilities

- Maintain and enhance the Tauri v2 theme studio application.
- Build and verify per-platform theme packagers (Windows `.deskthemepack`, macOS HEIC/soundpacks, Linux XDG cursor themes).
- Ensure the frontend studio UI operates cleanly with Svelte 5 runes and token-driven SCSS.
- Maintain zero-warning quality gates across Rust and frontend builds.

---

## 2. Invariants

- Never commit generated build artifacts (`build/`, `target/`).
- Rust code must compile with `RUSTFLAGS="-D warnings"` with 0 warnings.
- Frontend must pass `svelte-check` with 0 errors and 0 warnings.
- Read-only git operations strictly enforced.
