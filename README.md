# ianfoster.org

Ian Foster's personal site. Plain static HTML + one CSS file — no generator,
no build step, no JavaScript. Edit the HTML, push, done.

## Structure

- `index.html` — front page: short bio
- `writing/` — books and selected articles
- `about/` — longer bio and contact
- `style.css` — the only stylesheet
- `SETUP.md` — one-time DNS and hosting setup

## Conventions

- Content voice is Ian's; nothing goes live without his sign-off.
- Clean URLs via directory `index.html` files; absolute paths (`/style.css`) throughout.
- TODO: photo at `images/ian-foster.jpg` (placeholder markup commented out in `index.html`).

## Preview locally

    python3 -m http.server -d . 8000

then open http://localhost:8000.
