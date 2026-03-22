# Orthodox Map Static Snapshot

This folder is a standalone static map site powered by snapshot JSON files.

## Contents

- `index.html` - static map application (no backend required)
- `data/snapshots/*.json` - precomputed map data layers
- `.nojekyll` - ensures GitHub Pages serves files as-is

## Host On GitHub Pages

## Option 1: Publish from `main` using `/docs`

GitHub Pages on a branch supports only `/ (root)` or `/docs` as the source folder.

1. Copy the contents of this folder into `docs/`.
2. In GitHub, open **Settings -> Pages**.
3. Set **Source** to **Deploy from a branch**.
4. Set **Branch** to `main` and **Folder** to `/docs`.
5. Save and wait for Pages to build.

## Option 2: Publish with a `gh-pages` branch

1. Copy the contents of this folder to the root of a `gh-pages` branch.
2. In **Settings -> Pages**, set **Branch** to `gh-pages` and **Folder** to `/ (root)`.

## Option 3: Publish from root

1. Copy the contents of this folder to repository root.
2. In **Settings -> Pages**, set **Branch** to `main` and **Folder** to `/ (root)`.

## Local Preview

Use any static file server from repository root:

```powershell
npx serve gh-pages-map-static
```

Then open the URL shown by the server.

## Notes

- All data is loaded using relative paths (`./data/snapshots/...`), so it works under GitHub Pages project subpaths.
- The site is snapshot-only. It does not call backend `/api` endpoints.
