# Teddy Schwartz — personal website

A one-page, responsive site built with plain HTML and CSS. No JavaScript, build step, dependencies, or backend.

## Preview locally

From this directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. Stop the server with Ctrl+C. You can also open `index.html` directly.

## Edit content

- `index.html`: introduction, experience, paper descriptions, links, and contact details. Each work entry is a separate `<article>`.
- `styles.css`: typography, accent color, spacing, responsive styles, and keyboard focus.
- About: write your text inside `.about-copy`, then remove `hidden` from both `#about` and its navigation link. Keep both hidden while the section is empty.
- Update year of study and “Present” dates as needed.

## Assets

The supplied papers are included:

- `assets/papers/imitation-learning.pdf` — supplied junior paper.
- `assets/papers/training-partner-diversity.pdf` — supplied senior paper.

Their summaries are checked against the PDFs. They are labeled research papers, with no publication or acceptance claim.

The supplied résumé is included at `assets/resume/teddy-schwartz-resume.pdf`. Optional approved project screenshots can still be added.

### Résumé

Replace `assets/resume/teddy-schwartz-resume.pdf` to update the résumé. The introduction’s “Download résumé (PDF)” link uses the HTML `download` attribute.

### Screenshots

Put approved images in `assets/images/`, using simple names such as `lang-pipeline.png` or `youth-japan-events.png`. Add a figure inside the relevant work article:

```html
<figure>
  <img src="assets/images/lang-pipeline.png"
       alt="Describe what this actual screenshot shows"
       width="1200" height="800" loading="lazy">
  <figcaption>A short, factual caption for this screenshot.</figcaption>
</figure>
```

Use the image's actual dimensions and meaningful alt text. No screenshots or visible image placeholders are included because none were supplied.

## Static hosting

Serve `index.html`, `styles.css`, and `assets/` together from any static host. All local paths are relative. For GitHub Pages, the repository root can be the publishing source; no build is needed. Deployment is outside this task.

## Checks when editing

Preview at desktop and mobile widths (including 320px), confirm no horizontal overflow, and use Tab/Shift+Tab to check link order and visible focus. Open both paper links and the résumé after adding it. The Youth Japan “View site” destination intentionally remains `https://project-youth-japan.vercel.app/library`.

## Initial verification

Checked the local site in Chrome at desktop (1470px), 375px, and 320px widths; no horizontal overflow was found. Visually inspected the introduction, research entries, paper list, and contact section. Verified the skip link, keyboard focus, hidden About section, local anchor targets, and successful HTTP responses for the stylesheet and both PDFs. The copied PDFs match the supplied originals. Opened the exact Youth Japan library destination successfully. The résumé download link points to the supplied PDF, copied without modification.
