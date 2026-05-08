# Catalyst Intelligence

Internal strategy artifacts and intelligence infrastructure.
Catalyst Energy Africa — Sub-Saharan African energy and water infrastructure.

**Live:** https://catalystenergy.github.io/catalyst-intelligence/

---

## Structure

```
docs/                          ← GitHub Pages root (live URLs)
  index.html                   ← Landing page
  lifecycle-signal-map.html    ← Lifecycle Signal Intelligence Map (current)
  opportunity-scanner.html     ← Opportunity Scanner Dashboard (generated)

artifacts/
  lifecycle-signal-map/
    archive/                   ← Versioned snapshots
      v0.1.html                ← Original build (May 2026)
```

## Artifacts

| Artifact | Version | Live URL |
|---|---|---|
| Lifecycle Signal Intelligence Map | v0.1 | [/docs/lifecycle-signal-map.html](https://catalystenergy.github.io/catalyst-intelligence/lifecycle-signal-map.html) |
| Opportunity Scanner Dashboard | generated | [/docs/opportunity-scanner.html](https://catalystenergy.github.io/catalyst-intelligence/opportunity-scanner.html) |

## Versioning convention

**Lifecycle Signal Map** — version bumps on content changes (new layers, entry points, structural changes). CSS/layout fixes do not bump the version.

Before publishing a new version:
1. Archive the current file: `cp docs/lifecycle-signal-map.html artifacts/lifecycle-signal-map/archive/vX.X.html`
2. Update `docs/lifecycle-signal-map.html` with the new version
3. Update the version table above and the version log below
4. Commit and push

**Opportunity Scanner Dashboard** — generated from `opportunity-scanner` repo (private). Do not edit `docs/opportunity-scanner.html` directly.

To update:
```bash
cd ~/opportunity-scanner
python generate_dashboard.py
cp docs/index.html ~/catalyst-intelligence/docs/opportunity-scanner.html
cd ~/catalyst-intelligence
git add docs/opportunity-scanner.html
git commit -m "update: opportunity scanner dashboard — [description]"
git push
```

## Version log

### Lifecycle Signal Map
- **v0.1** (May 2026) — Two layers: canonical lifecycle phases + named signal sources. Entry point layer (L03) pending audit.

### Opportunity Scanner Dashboard
- Generated artifact — see `opportunity-scanner` repo for changelog.
