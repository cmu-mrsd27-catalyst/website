# Catalyst — MRSD Capstone Website

Static site — just HTML and CSS, no build tools.

## File Structure

```
├── index.html          Home — project overview, problem, system design, schedule
├── team.html           Team member bios (one card per person)
├── system.html         Subsystem status table + progress updates
├── documents.html      Links to presentations, reports, planning docs
├── media.html          Photo gallery
├── css/style.css       All styles
├── assets/
│   ├── images/         Team photos, diagrams, gallery photos
│   └── docs/           PDFs and documents
```

## Previewing Locally

Open the file directly:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
```

Or run a local server (useful if you later add anything that needs one):

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## How It Works

**Styling:** Single stylesheet at `css/style.css`. CMU red (`#C41230`) nav bar, max-width 900px centered layout, system fonts.

**Navigation:** Each page has the same `<nav>` bar. The current page's link gets `class="active"`. If you add or rename a page, update the nav in every HTML file.

**Documents (`documents.html`):** Flat list of links grouped by type. Point `href` to files in `assets/docs/` or external URLs.

**Gallery (`media.html`):** Each photo is a `<figure>` with an `<img>` and `<figcaption>` inside `.gallery`.

## Images

- Put files in `assets/images/`
- Reference as `assets/images/filename.jpg`
