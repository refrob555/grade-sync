# Grade Sync

Windows portable app for Rock Valley College instructors to compare LMS quiz scores with Eagle and optionally write updates.

**Current download:** see the [latest release](https://github.com/refrob555/grade-sync/releases) for `GradeSync-0.5.15-windows-portable.zip` (tip `9b29b92`).

SHA-256 of the 0.5.15 portable zip:

```
513b139018fecc1b0bf0ec48a20a14d67530c612aa187bde623a2024fd3579ba
```

See [CHANGELOG.md](CHANGELOG.md) for what changed from 0.5.14 → 0.5.15.

## What it covers

- **MEC-153** — LearnAmatrol quiz scores → Eagle
- **MEC-163** — LearnUpon exam scores → Eagle

Both paths stay in the same portable build. Pick the Eagle class; the app chooses the matching LMS sign-in.

## Run the portable (Windows)

1. Download `GradeSync-0.5.15-windows-portable.zip` from [Releases](https://github.com/refrob555/grade-sync/releases).
2. Unzip to a folder you can write to.
3. Double-click **Start grade sync.bat** (or the Start shortcut in that folder).
4. The teacher page opens locally in Edge (Chrome if Edge is missing), typically at `http://127.0.0.1:47621`.

## Safety

- **Propose / Load before Write.** Load compares scores and does not post grades.
- Incomplete / NS stay blank — they are never written as `0`.
- Lab answer sheets are not posted as quiz scores.
- Sign-in uses a browser window you control. Passwords are not saved in the portable for the teacher UI path.
- Do not commit `.env`, tokens, API keys, MFA secrets, or student PII into this repo.

## Screenshots

Scrubbed home and results (no student names/IDs):

### MEC-153 (Amatrol)

![MEC-153 home](docs/screenshots/mec153-home.png)

![MEC-153 results](docs/screenshots/mec153-results.png)

### MEC-163 (LearnUpon)

![MEC-163 home](docs/screenshots/mec163-home.png)

![MEC-163 results](docs/screenshots/mec163-results.png)

## Source of truth

Active development for this tool lives on Cursor Origin (`robert-fricke/amatrol-eagle-grade-transfer`). This GitHub repo is the **public download home** (README + release assets).

## License / use

Intended for Rock Valley College Automation instructors using Eagle with Amatrol or LearnUpon. No credentials are distributed with the zip.
