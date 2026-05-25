# Publish Serendipity to Obsidian Community Themes

## Repository checklist

- [x] `manifest.json` at repo root (name must match theme folder: **Serendipity**)
- [x] `theme.css` at repo root — **Serendipity Morning** (light) + **Serendipity Midnight** (dark)
- [x] `screenshot.png` — 512×288 preview
- [x] `versions.json` — maps `1.0.0` → `1.0.0`
- [x] `README.md` and `LICENSE`


Extra variants (CSS snippets):

- `serendipity-sunset.css` — CSS snippet in `variants/`

## GitHub release

1. Create release tag **`1.0.0`** (must match `manifest.json` version).
2. Attach **`manifest.json`** and **`theme.css`** as release assets.
3. Push tag: `git tag 1.0.0 && git push origin 1.0.0`

Or with GitHub CLI:

```bash
gh release create 1.0.0 manifest.json theme.css --title "1.0.0" --notes "Initial community theme release."
```

## Submit

1. Sign in at [community.obsidian.md](https://community.obsidian.md) with your Obsidian account.
2. Link your GitHub account in profile settings.
3. **Themes → New theme** → enter `https://github.com/Serendipity-Theme/obsidian`.
4. Agree to developer policies and submit.

Obsidian reads `manifest.json` from the default branch and installs `theme.css` + `manifest.json` from the GitHub release matching the manifest version.

## Updates

Bump `version` in `manifest.json`, add the new version to `versions.json`, commit, and create a new tagged release with updated assets.
