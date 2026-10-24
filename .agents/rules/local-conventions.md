# Local Conventions — theme-toolkit (Theme Studio)

> Authoritative conventions for `theme-toolkit` (**Theme Studio**).
> Pure native C++20 Windows desktop application targeting Windows exclusively, supporting **Windows 2000 all the way to Windows 11+**.

---

## 1. Platform & Toolchain

- **Platform Target:** Windows exclusively. Full theme compatibility spanning Windows 2000, XP, Vista, 7, 8, 8.1, 10, and 11+.
- **Language Standard:** C++20 standard; MSVC compiler.
- **Compiler Warnings:** MSVC `/W4` with warnings treated as errors (`/WX`). Zero warnings invariant strictly enforced.

---

## 2. Multi-Version Windows Theme Packaging Invariants

- **Windows 2000 & XP:** Legacy `.theme` files with `[Control Panel\Colors]`, `[Control Panel\Desktop]`, and `[Metrics]`.
- **Windows Vista & 7:** Aero glass `.themepack` archives (CAB-compressed `.theme` bundles with wallpaper slideshows and sound schemes).
- **Windows 8, 10 & 11+:** Modern `.deskthemepack` archives generated via MSVC `makecab.exe /F <theme>.ddf`.
- **Asset Validation:** All wallpaper images, cursor assets (`.cur`, `.ani`), and sound events (`.wav`) must pass integrity checks before packaging.

---

## 3. UI & Direct2D Standards

- Direct2D / DirectWrite hardware-accelerated studio canvas for real-time theme previews with simulated OS version skins.
- Windows 11 dark mode integration via `DwmSetWindowAttribute(hwnd, DWMWA_USE_IMMERSIVE_DARK_MODE, ...)`.
- Per-Monitor V2 DPI awareness.
