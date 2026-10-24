# theme-toolkit — Task Checklist & Workstream Tracking (Theme Studio)

> 📋 **Living Source of Truth**: Actionable task ledger for **theme-toolkit** (**Theme Studio**).
> Statuses: ⬜ backlog · 🚧 in progress · ✅ done (tracked as `- [ ]` and `- [x]` checkboxes).
> High-level direction lives in [`ROADMAP.md`](./ROADMAP.md), active sprints in [`PLAN.md`](./PLAN.md), issues in [`BUGS.md`](./BUGS.md).

---

## 📜 Tracking Rules

- **100% Active Direction Accuracy**: Task items and checklists must reflect the current state of Theme Studio with zero contradictions.
- **Normalized Directives**: Rewrite user directives into clean, self-contained engineering requirements.
- **Done Moves Down**: Completed items are marked with `- [x]` and collapsed to minimal one-line entries under completed workstreams.
- **Zero-Warning Gate**: All builds and tests must pass with 0 errors and 0 warnings under MSVC `/W4 /WX`.

---

## 🔥 Active Workstreams

### 🎯 [theme-toolkit] Workstream W.01: Native Windows C++ Architecture & Rebrand to Theme Studio (v1.0.0)
- **Project Identifier:** `[theme-toolkit]`
- **Repository Path:** `projects/theme-toolkit`
- **Status:** 🚧 In progress. Abandon Tauri v2 rewrite; rebrand to Theme Studio; pivot to pure native C++ Windows desktop app supporting Windows 2000 to Windows 11+.
- **Target Component:** Native C++ Core & Direct2D Win32 UI

**Locked user directives (normalized by domain):**
- **Rebrand to Theme Studio**: The application is officially rebranded to **Theme Studio** as part of its native C++ rewrite.
- **Universal Windows Version Spectrum**: Support everything from **Windows 2000 all the way to Windows 11+**:
  - Legacy Windows 2000 / XP: Classic `.theme` files, SysColors, metrics, and visual style pointers.
  - Windows Vista / 7: Aero glass parameters, `.themepack` archives, desktop slideshows, custom sounds.
  - Windows 8 / 8.1: Flat accent colorization, modern `.deskthemepack` CAB packaging.
  - Windows 10 / 11+: Modern `.deskthemepack`, dark/light theme switching, accent palette harmonies, and Mica/Acrylic backdrop awareness.
- **Abandon Tauri Rewrite**: Cease development on the Tauri v2 / Rust / SvelteKit stack.
- **Pure Windows Desktop**: Focus 100% on native Windows desktop execution; drop macOS and Linux cross-platform scope entirely.
- **Multi-Format Packager**: Support legacy `.theme`, Windows 7 `.themepack`, and Windows 8/10/11+ `.deskthemepack` via MSVC `makecab.exe` integration.
- **Windows Sound Scheme Manager**: Win32 Sound Event mapping and `.wav` audio preview / bundling.
- **Wallpaper & Slideshow Studio**: Desktop background viewport, slideshow interval / shuffle controls, alignment settings.
- **Windows Cursor Scheme Inspector**: 15 standard Win32 cursor role configuration with `.ani` and `.cur` frame previews.
- **Direct2D Studio Canvas**: Hardware-accelerated native Win32 UI with real-time theme previews.

**Implementation checklist:**
- [ ] **[theme-toolkit] 1. Native C++ Win32 Project Scaffold**:
  - [ ] `[theme-toolkit]` Author native CMake build configuration with MSVC `/W4 /WX` C++20 standard.
  - [ ] `[theme-toolkit]` Build main Win32 application window with Windows 11 dark mode frame.
  - [ ] `[theme-toolkit]` Implement hardware-accelerated Direct2D / DirectWrite studio canvas.
- [ ] **[theme-toolkit] 2. Multi-Version Windows Theme Engine (Win 2000 → 11+)**:
  - [ ] `[theme-toolkit]` Implement legacy Windows 2000/XP `.theme` generator with SysColors and metric mappings.
  - [ ] `[theme-toolkit]` Implement Windows Vista/7 Aero `.themepack` generator with glass parameters and slideshows.
  - [ ] `[theme-toolkit]` Implement Windows 8/10/11+ `.deskthemepack` packager generating `.ddf` and invoking `makecab.exe`.
  - [ ] `[theme-toolkit]` Implement Win32 Sound Scheme `.wav` mapper and packer.
  - [ ] `[theme-toolkit]` Implement Win32 Cursor Scheme (`.cur` / `.ani`) validator and packer.
- [ ] **[theme-toolkit] 3. Native Studio UI & Preview Canvas**:
  - [ ] `[theme-toolkit]` Real-time interactive theme preview canvas supporting simulated preview in Win2K, Win7 Aero, and Win11 styles.
  - [ ] `[theme-toolkit]` Color picker and contrast accessibility evaluator.
- [ ] **[theme-toolkit] 4. Quality Gate & Packaging**:
  - [ ] `[theme-toolkit]` Verify 0 compiler warnings under MSVC `/W4 /WX`.
  - [ ] `[theme-toolkit]` Verify generated theme archives apply cleanly across target Windows versions.

---

## ✅ Completed Workstreams

- _(Initial workstream in progress)_
