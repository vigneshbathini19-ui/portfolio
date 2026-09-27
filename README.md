# Bathini Vignesh — Portfolio

A clean, recruiter-friendly personal portfolio built with plain HTML, CSS, and
JavaScript — no framework or build step required.

## Project structure

```
portfolio/
├── index.html                 # All page sections
├── css/
│   └── style.css              # All styling (design tokens at the top)
├── js/
│   └── script.js              # Mobile nav toggle + expandable project cards
├── render.yaml                # Render Blueprint (static site)
├── PLACE_RESUME_HERE.txt      # Reminder — see "Add your resume" below
└── README.md
```

## 1. Install dependencies

There are none — this is a static site with no build tooling. You just need
a way to serve static files locally (see below).

## 2. Run locally

Any static file server works. For example, with Python:

```bash
cd portfolio
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

Or with Node's `serve`:

```bash
npx serve .
```

## 3. Build the project

No build step is needed — `index.html`, `css/style.css`, and `js/script.js`
are served as-is.

## 4. Deploy to Render

1. Push this project to a GitHub (or GitLab) repository.
2. In Render, choose **New > Blueprint** and point it at the repository.
   Render will read `render.yaml` and configure a static site automatically.
3. Alternatively, choose **New > Static Site** manually and set:
   - **Build Command:** (leave empty, or `echo "No build step required"`)
   - **Publish Directory:** `.`

## 5. Add your resume

Place your resume PDF in this folder and name it `resume.pdf`, so the final
deployed URL is `/resume.pdf`. The "Download Resume" buttons in the navbar
and hero section already link there — see `PLACE_RESUME_HERE.txt`.

## 6. Update personal information

Personal details (name, email, phone, LinkedIn, GitHub) appear in a few
places in `index.html`:
- The hero section (`<section class="hero">`)
- The contact section (`<section id="contact">`)
- The footer (`<footer class="footer">`)
- The `<title>` and `<meta name="description">` tags in `<head>`

## 7. Add real GitHub project URLs

Each project card in the "Projects" section
(`<section id="projects">`) has a **GitHub** button:

```html
<a href="https://github.com/BathiniVignesh" target="_blank" rel="noopener noreferrer" class="btn btn--small btn--outline">GitHub</a>
```

Replace the `href` with the specific repository URL for that project once
it's public.

## 8. Add real live-demo URLs

Each project card also has a disabled **Live Demo (coming soon)** link.
Once a project has a real deployed URL, replace it with a working link, for example:

```html
<a href="https://your-live-demo-url.com" target="_blank" rel="noopener noreferrer" class="btn btn--small btn--outline">Live Demo</a>
```

and remove the `aria-disabled="true"` attribute and the `btn--ghost` class,
using `btn--outline` instead (matching the GitHub button style).

## Notes

- All content reflects only what was provided — no invented experience,
  companies, links, or metrics.
- Colors, spacing, and type scale are defined as CSS custom properties at the
  top of `css/style.css` if you want to adjust the look.
