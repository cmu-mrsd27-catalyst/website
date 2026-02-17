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

**Placeholders:** Anything with `class="placeholder"` renders with a yellow dashed border. Remove the class when you replace it with real content.

**Team cards (`team.html`):** Each person is a `<div class="team-card">` inside the `.team-grid`. Photos display as circles — use roughly square images.

**Status badges (`system.html`):** Three styles for the subsystem table:
```html
<span class="status status-done">Complete</span>
<span class="status status-wip">In Progress</span>
<span class="status status-todo">Not Started</span>
```

**Progress updates (`system.html`):** Add new update sections at the top so the most recent appears first.

**Documents (`documents.html`):** Flat list of links grouped by type. Point `href` to files in `assets/docs/` or external URLs.

**Gallery (`media.html`):** Each photo is a `<figure>` with an `<img>` and `<figcaption>` inside `.gallery`.

## Images

- Put files in `assets/images/`
- Reference as `assets/images/filename.jpg`
- Team photos: square-ish (they crop to circles)
- Gallery photos: any aspect ratio (they crop to 4:3)

## Git Workflow

```bash
git pull
# make edits
git add -A
git commit -m "description of change"
git push
```
