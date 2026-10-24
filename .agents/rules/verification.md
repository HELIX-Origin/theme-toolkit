# Verification Gate — theme-toolkit (Theme Studio)

> Authoritative verification gate for `theme-toolkit` (**Theme Studio**).
> All compilers and linters must pass with zero errors and zero warnings (`/W4 /WX`).

---

## 1. Native Build & Test Verification

```powershell
# 1. Native C++ build — MSVC warning level /W4 with warnings treated as errors (/WX)
cmake -B build -S . -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release

# 2. Native unit test suite (Deskthemepack packager & DDF generator)
ctest --test-dir build -C Release --output-on-failure
```

---

## 2. Quality Gate Invariants

- Every compilation step must produce **0 errors and 0 warnings** under MSVC `/W4 /WX`.
- All packaging tests and theme validator checks must pass cleanly.
