# Architecture — theme-toolkit (Theme Studio)

> Authoritative architectural specification for `theme-toolkit` (**Theme Studio**).
> Native C++20 Windows desktop theme studio and applicator.

---

## 1. Directory Structure (Target Native Layout)

```
theme-toolkit/
├── CMakeLists.txt              # Top-level native CMake build definition
├── src/
│   ├── app/                    # Win32 Application Lifecycle
│   │   ├── main.cpp            # WinMain entry point
│   │   ├── app_window.cpp/.h   # Main studio window & message loop
│   │   └── dpi_helper.cpp/.h   # Per-Monitor V2 DPI scaling
│   ├── ui/                     # Direct2D Studio Canvas & Controls
│   │   ├── studio_canvas.cpp/.h# Hardware-accelerated theme preview
│   │   ├── color_picker.cpp/.h # Palette editor & contrast evaluator
│   │   ├── cursor_panel.cpp/.h # Win32 cursor inspector (.cur/.ani)
│   │   ├── sound_panel.cpp/.h  # Win32 sound scheme manager (.wav)
│   │   └── wallpaper_panel.cpp/.h # Background & slideshow preview
│   ├── packager/               # Windows Theme Packaging Engine
│   │   ├── ddf_generator.cpp/.h# Diamond Directive File (.ddf) writer
│   │   ├── makecab_runner.cpp/.h # makecab.exe invocation & verification
│   │   └── theme_writer.cpp/.h # .deskthemepack & .theme file generator
│   └── core/                   # Theme Data Models & Validation
│       ├── theme_schema.cpp/.h # Color, sound, cursor, and wallpaper data
│       └── asset_validator.cpp/.h # Image dimension & file integrity checks
└── packaging/                  # Installer & release manifests
    └── installer.nsi           # Native Windows installer
```

---

## 2. Invariants

- Pure native C++20 Win32 application.
- Windows exclusively (Windows 11 / Windows 10).
- Direct2D / DirectWrite UI rendering.
