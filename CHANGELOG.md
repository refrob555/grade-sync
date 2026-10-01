# Changelog

## 0.5.14 → 0.5.15

**Release tip:** `9b29b92f2898f58ed73a9ef561a8aeb14f3d6180`  
**Portable zip SHA-256:** `513b139018fecc1b0bf0ec48a20a14d67530c612aa187bde623a2024fd3579ba`

### Highlights

- **Write buttons visible after Load** (parity with MEC-153): Write / Write grades with zeros / Remove all zeros (`ad38c540` lineage).
- **Reliable long Writes:** progress await ceiling 180s; on progress timeout warn and continue instead of aborting the remaining batch (`8014e26`).
- **No bare HTTP 502 / dead UI on Write:** LearnUpon `TimeoutError` during refresh caught and returned as JSON; non-daemon request threads; log flush (`a15ecdf`).
- **Verified:** MEC-163 Write prove — 51/51 would-post written, then clerk-restored blank (no lasting Eagle changes). Write verify PASS on `a15ecdf`.

### Also

- Packaging/version label **0.5.15** (`9b29b92`; packaging-only vs `a15ecdf`).
- Both LMS paths: Amatrol (MEC-153) + LearnUpon (MEC-163).

### Not changed

- Load / propose-only still does not write.
- Labs stay manual; incompletes are not invented as zeros.
