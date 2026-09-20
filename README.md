# Blurt Board — site

The marketing, support and privacy pages for **Blurt Board**, a soundboard for
iPhone, iPad, Mac and Apple Watch.

Three static pages, no build step, served by GitHub Pages.

| Page | Purpose |
| --- | --- |
| `index.html` | Landing page — App Store Connect *Marketing URL* |
| `support.html` | Common questions and contact — Connect *Support URL* (required) |
| `privacy.html` | Privacy policy — Connect *Privacy Policy URL* (required) |

App Review opens the support and privacy URLs, so neither may 404.

## Editing

Plain HTML with one shared `style.css`. Check locally before pushing:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Contact address

Every page uses **blurtboard.app@gmail.com**, a dedicated account rather than a
personal one — the address here is indexed and permanent. To change it:

```bash
sed -i '' 's/blurtboard\.app@gmail\.com/new@example.com/g' *.html
grep -o 'mailto:[^"]*' *.html | sort -u    # confirm every page moved
```

Keep it matching the support contact in App Store Connect.

## Screenshot

`mac-board.png` comes from the app's own screenshot set. If the app's look
changes enough to matter, replace it rather than letting the site show an old
build.

## Source

These pages live in the app's own repository under `Docs/Site/` and are copied
here to publish. Edit them there and copy across, or edit here and copy back —
but do not let the two drift.
