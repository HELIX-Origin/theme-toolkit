# theme-toolkit (Theme Studio)

Native C++ Windows desktop theme studio and applicator (**Theme Studio**).
Supports everything from **Windows 2000 all the way to Windows 11+**.
Pure native Windows application targeting Windows exclusively. Rebranded from Theme Toolkit to Theme Studio as part of its native C++ rewrite. MIT license.

## Architecture at a glance

- **Native Windows C++ Application (Theme Studio):** Tauri v2 cross-platform stack abandoned in favor of a lean, high-performance native C++20 Win32 application.
- **Universal Windows Version Support (Win2K to Win11+):**
  - Legacy `.theme` files and classic SysColor metrics (Windows 2000, XP).
  - Windows Vista & 7 Aero `.themepack` archives, desktop slideshows, and sound schemes.
  - Windows 8 / 8.1 auto-colorization and modern `.deskthemepack` archives.
  - Windows 10 & 11+ Fluent palettes, dark/light mode toggles, Mica/Acrylic accents.
- **Hardware-Accelerated Studio UI:** Direct2D / DirectWrite theme editor canvas with real-time preview across Windows version profiles, token mapping, and instant packager.
- **Zero-Warning Invariant:** MSVC `/W4 /WX` enforced across all targets.

## Build & test

| Command / Tool | Purpose |
|---|---|
| MSVC `cl.exe` / `cmake --build` | Native C++20 compilation with `/W4 /WX` (warnings as errors) |
| `ctest` / test runner | Run native unit and packaging tests |

## Conventions (summary)

- **Platform:** Windows exclusively; backwards compatible from Windows 2000 to Windows 11+.
- **C++:** C++20 standard; MSVC warning level `/W4 /WX`.
- **Packaging:** Native `.theme`, `.themepack`, and `.deskthemepack` via MSVC `makecab.exe` directives.

See `.agents/rules/local-conventions.md` and `.agents/rules/verification.md` for complete guidelines.

## Invariants

MIT license · SemVer releases · zero-warning builds (`/W4 /WX`) · community-health files · universal Windows theme compatibility.
