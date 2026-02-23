# Plan: Full replacement clone from `C:\Users\staud\Desktop\sumisite` to `suomipelit.games`

## 1) Objective and constraints
- Replace the current project site code entirely with a migrated copy of `C:\Users\staud\Desktop\sumisite`.
- Use new naming across all pages.
- Standardize legacy host references to `suomipelit.games`.
- Preserve legacy functionality and local `_files` asset behavior while normalizing filenames and routes.

## 2) Source inventory
- Root HTML files in legacy snapshot:
  - `Suomitop20.html`
  - `about.html`
  - `Bloodaxe.html`
  - `Book of Cleo.html`
  - `Rooster Mobs Slot.html`
  - `Privacy Policy.html`
  - `Terms of Use.html`
- Per-page asset folders: `Suomitop20_files`, `about_files`, `Bloodaxe_files`, `Book of Cleo_files`, `Rooster Mobs Slot_files`, `Privacy Policy_files`, `Terms of Use_files`.

## 3) Replacement strategy (no merge)
- Full copy replaces existing project files.
- Existing pages in this repo are not merged/combined; they are replaced in one pass using new names.

## 4) New naming and route map
Use file names that are clean, URL-safe, and unambiguous:

- `index.html` ← from `Suomitop20.html`
- `about.html` ← from `about.html` (optionally rename to `about-us.html` in links if desired)
- `games/bloodaxe.html` ← from `Bloodaxe.html`
- `games/book-of-cleo.html` ← from `Book of Cleo.html`
- `games/rooster-mobs-slot.html` ← from `Rooster Mobs Slot.html`
- `privacy-policy.html` ← from `Privacy Policy.html`
- `terms-of-service.html` ← from `Terms of Use.html`

Notes:
- This keeps one clear namespace and removes legacy spacing/case issues.
- If you want top-level files instead of `games/`, map to `bloodaxe.html`, `book-of-cleo.html`, `rooster-mobs-slot.html` and remove `games/` folder.
- Legacy filenames are removed from the final route surface.

## 5) Directory and asset plan
- Copy each page’s corresponding `_files` folder to match its new route location.
- Keep relative assets exactly where needed so existing JS/CSS/image/script references continue to work.
- If a page moves into `games/`, keep the page’s `_files` folder either:
  - beside the moved page under `games/` (preferred), or
  - mirrored at root and update asset paths explicitly.
- Prefer the first option (co-located assets) for less path churn.

## 6) Domain migration rules
- Replace all hardcoded legacy domain references:
  - `https://suomitop20.games` -> `https://suomipelit.games`
  - `http://suomitop20.games` -> `https://suomipelit.games`
  - bare `suomitop20` references in link paths -> `suomipelit.games`
- Update canonical and footer links to new domain and host paths.

## 7) About / Terms / Privacy updates (“new naming”)
- Apply new filenames from section 4.
- Update internal links to these pages to use:
  - `/about.html` (or `/about-us.html` if chosen)
  - `/privacy-policy.html`
  - `/terms-of-service.html`
- Update visible text references from “Privacy Policy” / “Terms of Use” only if needed for branding consistency.

## 8) Link/path normalization
- Resolve legacy links:
  - `pipindex.html` → `/index.html`
  - `g1.html`, `g2.html`, `g4.html` → new game page routes above
- Normalize all remaining relative paths and avoid raw spaces in paths.

## 9) Quick QA (after replacement)
- Global search for stale domain references:
  - `suomitop20`
  - old file names with spaces
- Confirm the following routes resolve to new names:
  - `/`, `/about`, `/privacy-policy`, `/terms-of-service`, `/games/bloodaxe`, `/games/book-of-cleo`, `/games/rooster-mobs-slot`
- Validate that embedded resources and iframes load from new locations.

## 10) Acceptance criteria
- Project contains no merge-originated legacy naming collisions from the previous site version.
- All old site functionality visible in new routes with `suomipelit.games` branding/links.
- About/Terms/Privacy page filenames updated to the new naming convention.
