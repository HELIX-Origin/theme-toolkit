# theme-toolkit — Task Checklist & Workstream Tracking

> 📋 **Living Source of Truth**: Actionable task ledger for **theme-toolkit**.
> Statuses: ⬜ backlog · 🚧 in progress · ✅ done (tracked as `- [ ]` and `- [x]` checkboxes).
> High-level direction lives in [`ROADMAP.md`](./ROADMAP.md), active sprints in [`PLAN.md`](./PLAN.md), issues in [`BUGS.md`](./BUGS.md).

> [!IMPORTANT]
> AI agents are strictly required to update this page and related tracking ledgers **before** executing new feature work or bug fixes and keep them synchronized.

---

## 📜 Tracking Rules

- **No Typo Duplication**: When recording user reports, clean and fix all typos to preserve professional quality.
- **Consistent Formatting**: Maintain consistent formatting and style throughout all documentation to ensure readability and professionalism.
- **Clear Sectioning**: Use clear and descriptive headers for each section to improve navigation and readability.
- **Active Items First**: The currently active milestone, sprint, task, or workstream must always be placed at the top of the content sections.
- **Regular Updates**: Ensure that this file is regularly updated to reflect the latest developments and changes in the project.
- **Improve & Categorize User Directives**: Rewrite user directives into clean, self-contained engineering requirements grouped by domain sub-headers (e.g., **Architecture & Plugins**, **UI & Icons**, **Data & Cache**) so it is immediately clear what goes to what. Never dump raw chronological chat quotes or leave contradictory superseded statements.
- **100% Active Direction Accuracy**: Whenever a requirement pivots or supersedes an earlier decision, replace the superseded directive in place across `ROADMAP.md`, `PLAN.md`, `TODO.md`, and `BUGS.md`.
- **Same-Change Updates**: When a task changes behavior or scope, update this file **in the same change**.
- **Done Moves Down**: When a workstream is done, check it off and archive detailed checklists to `.github/TODO-ARCHIVE.md`, leaving a concise single-line summary under Completed Workstreams.
- **Explicit Project Tagging**: In multi-project or organization tracking ledgers, every workstream header, checklist group, and individual checkbox item MUST be explicitly prefixed with its project name and repository path (e.g., `[theme-toolkit] (theme-toolkit)` or `- [ ] [theme-toolkit] ...`) to prevent agent context confusion.
- **Tracking Docs Stay True**: Update `ROADMAP.md`, `TODO.md`, `BUGS.md`, and `PLAN.md` first or in lockstep with code changes.
- **Always Track Everything**: Every new feature request, enhancement, or bug report must be logged before execution.

---

## 🔥 Active Workstreams

### [theme-toolkit] Workstream W.01: Theme Studio Core Features
- **Project Identifier:** `[theme-toolkit]`
- **Repository Path:** `theme-toolkit`
- **Target Component:** Core Architecture

**Locked user directives (normalized by domain):**
- **Packaging:** Makecab & DDF Packaging Engine - Rust engine generating Diamond Directive Files (`.ddf`) and executing `makecab.exe`.
- **Sound:** Sound Scheme Manager - Win32 Sound Event mapping and `.wav` audio preview / bundling.
- **Wallpaper:** Wallpaper & Slideshow Studio - desktop background viewport, slideshow interval / shuffle controls, alignment settings.
- **Cursor:** Cursor Scheme Inspector - 15 standard Win32 cursor role configuration with `.ani` and `.cur` frame previews.
- **Visual Style:** Color & Visual Style Editor - real-time DWM accent colorization and dark/light system mode toggles.
- **macOS:** macOS Native Tooling (`macos.rs`) - Dynamic Desktop timed/solar HEIC wallpaper generator, system alert `.soundpack` archiver, cursor bundle packager.
- **Linux:** Linux Native Tooling (`linux.rs`) - FreeDesktop Sound Theme audio packager, XDG cursor and icon theme packager, desktop background XML generator (GNOME, KDE Plasma, XFCE, Cinnamon).
- **UI:** Frontend Studio UI - interactive previews (wallpaper viewport, audio player, animated cursor canvas, real-time color pickers).

**Implementation checklist:**
- [x] `[theme-toolkit]` **Core Tauri v2 Scaffolding** - Tauri v2 app with SvelteKit frontend and Rust backend.
- [ ] `[theme-toolkit]` **Makecab & DDF Packaging Engine** - Rust engine generating `.ddf` and executing `makecab.exe`.
- [ ] `[theme-toolkit]` **Sound Scheme Manager** - Win32 Sound Event mapping and `.wav` audio preview / bundling.
- [ ] `[theme-toolkit]` **Wallpaper & Slideshow Studio** - desktop background viewport, slideshow interval / shuffle controls, alignment settings.
- [ ] `[theme-toolkit]` **Cursor Scheme Inspector** - 15 standard Win32 cursor role configuration with `.ani` and `.cur` frame previews.
- [ ] `[theme-toolkit]` **Color & Visual Style Editor** - real-time DWM accent colorization and dark/light system mode toggles.
- [ ] `[theme-toolkit]` **macOS Native Tooling (`macos.rs`)** - Dynamic Desktop HEIC generator, `.soundpack` archiver, cursor bundle packager.
- [ ] `[theme-toolkit]` **Linux Native Tooling (`linux.rs`)** - FreeDesktop Sound Theme packager, XDG cursor/icon packager, desktop background XML generator.
- [ ] `[theme-toolkit]` **Frontend Studio UI** - interactive previews (wallpaper viewport, audio player, animated cursor canvas, color pickers).
- [ ] `[theme-toolkit]` **Validation & Verification** - run project quality gate with zero warnings.

---

## ⬜ Backlog / Candidate Tasks

- [ ] [theme-toolkit] **Theme Toolkit User Manuals** - Author user manuals for theme-toolkit authoring, previewing, and packaging workflows (in docs repo).
- [ ] [theme-toolkit] **Theme Studio CI Deployment** - Create .github/workflows/ci.yml tailored for desktop theme applicator.

---

## ✅ Completed Workstreams & Archive

### ✅ [theme-toolkit] Workstream {{PREV_WORKSTREAM_ID}}: {{PREV_WORKSTREAM_TITLE}} ({{COMPLETED_DATE_OR_VERSION}})
- **Project Identifier:** `[theme-toolkit]`
- **Repository Path:** `theme-toolkit`

- [x] `[theme-toolkit]` {{COMPLETED_TASK_1}}
- [x] `[theme-toolkit]` {{COMPLETED_TASK_2}}
- [x] `[theme-toolkit]` {{COMPLETED_TASK_3}}

---

## 🔖 Metadata

- **Project**: theme-toolkit
- **Tracking Status**: {{STATUS_SUMMARY}}
