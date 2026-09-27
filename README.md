# thaiquoctoanvn.github.io

**🔗 Live site: [thaiquoctoanvn.github.io](https://thaiquoctoanvn.github.io)**

Portfolio of Android apps by Toan Thai, in a Neo-Brutalism style. Static site on GitHub Pages: a single `index.html`, no build step.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole page (CSS, JS and favicon inlined) |
| `apps.json` | All content: profile and app list |
| `avatar.jpg` | Profile photo |
| `readme/` | SVG card and buttons for the GitHub profile README |
| `.nojekyll` | Serve files as-is (no Jekyll) |

## Add or edit an app

Edit `apps.json`, then commit and push. No code changes needed.

```json
{
  "name": "App name",
  "featured": false,
  "playStoreUrl": "https://play.google.com/store/apps/details?id=...",
  "icon": "https://...",
  "description": "...",
  "tech": ["Jetpack Compose", "Hilt"],
  "screenshots": ["https://..."]
}
```

Optional fields: `tagline`, `category`, `downloads`, `rating`, `released`, `role`. `featured: true` pins the app first.

## Run locally

```sh
python3 -m http.server
```

Then open http://localhost:8000. Opening the file directly (`file://`) won't work because the page fetches `apps.json`.

Handy URL params: `?theme=dark`, `?state=loading`, `?state=error`.
