# Catalyst — MRSD Capstone Website

Static site — edit with LLMs.

1. Find the `.html` page you want to change
2. Dump it into an LLM with your requested changes
3. Preview locally: `python3 -m http.server 8000`
4. Make sure it looks good
5. Push to `main`

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

**Styling:** Single stylesheet at `css/style.css`.

**Documents (`documents.html`):** Flat list of links grouped by type. Point `href` to files in `assets/docs/` or external URLs (like in Google Drive)

## Images

- Put files in `assets/images/`
- Reference as `assets/images/filename.jpg`
