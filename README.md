# Rabotka — Pitch Deck

An interactive, browser-based pitch deck for **Rabotka**, a WhatsApp-based job platform for informal workers in African cities (starting with Brazzaville, Congo).

The deck is a self-contained static site — plain HTML, CSS, and vanilla JavaScript with no build step.

## 🔗 Live Deck

Once deployed, the deck is available at:

```
https://brx-hashcode.github.io/rabotka-pitch/
```

## Project Structure

| Path | Purpose |
|------|---------|
| `index.html` | The deck markup, styles, and slide content |
| `deck-stage.js` | Slide stage / navigation engine |
| `image-slot.js` | Image slot rendering and management |
| `support.js` | Shared runtime helpers loaded before the deck |
| `assets/` | Logos and static brand assets |
| `screenshots/` | Product screenshots used in slides |
| `uploads/` | User-provided imagery |

## Running Locally

Because it's a static site, any local web server works. From the project root:

```bash
# Python 3
python -m http.server 8000

# or Node (npx)
npx serve .
```

Then open <http://localhost:8000>.

> Opening `index.html` directly via `file://` may break relative script/asset loading in some browsers — prefer a local server.

## Navigation

- **Arrow keys** / on-screen controls to move between slides.
- The deck respects `prefers-reduced-motion` — animations are disabled and the final layout is shown for print and reduced-motion users.

## Deployment

The deck deploys automatically to **GitHub Pages** on every push to `main` via the workflow in [.github/workflows/deploy.yml](.github/workflows/deploy.yml).

### One-time setup

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.

After the next push to `main`, the deck will be published at the URL above.
