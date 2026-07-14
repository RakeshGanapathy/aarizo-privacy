# aarizo-privacy

Public Privacy Policy for [Aarizo](https://github.com/RakeshGanapathy/Aarizo), hosted as a static
site on GitHub Pages. This is the URL submitted to Google Play Console's Data Safety / Privacy
Policy field.

Pure HTML + CSS. No JavaScript, no analytics, no trackers, no cookies, no build step.

## Structure

```
/
├── index.html          # the policy page
├── styles.css           # all styling
├── assets/
│   └── aarizo-logo.svg  # inline app logo, vector, no raster export needed
└── README.md
```

## Updating the policy

The content here must always match the in-app Privacy Policy screen
(`app/src/main/java/com/aarizo/app/presentation/screens/settings/PrivacyPolicyScreen.kt` and the
`privacy_*` strings in `app/src/main/res/values/strings.xml` in the main Aarizo repo).

To update:

1. Edit `index.html` directly — each section maps 1:1 to a section in the in-app screen
   (Privacy at a Glance, Your Data, Permissions, AI, Backup & Encryption, Your Control).
2. Update the "Last Updated" date in the `<p class="doc-meta">` line whenever content changes.
3. Commit and push to `main` — GitHub Pages redeploys automatically within a minute or two.
4. If the in-app copy changes first, mirror the change here in the same PR/commit so the two never
   drift apart — Play Store review checks that the public policy matches actual app behavior.

## GitHub Pages configuration

Pages is served from the `main` branch, root (`/`) folder, via **Settings → Pages** in this
repository. No custom domain is configured — the published URL is:

```
https://rakeshganapathy.github.io/aarizo-privacy/
```

HTTPS is enforced automatically by GitHub Pages; no server or backend is required.
