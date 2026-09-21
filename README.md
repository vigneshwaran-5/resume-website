# Vigneshwaran Ravichandran — Resume Website

A fast, accessible, single-page portfolio site for Vigneshwaran Ravichandran,
Senior Software Engineer and Python Generative AI Engineer.

## Live site

Not yet deployed. Add the GitHub Pages URL here once the site is published
(see [Deployment](#deployment)).

## Features

- Responsive single-page layout tuned for mobile, tablet, and desktop
- Vertical experience timeline with separate entries for each role
- Selected AI work presented as experience-derived case studies
- Contact CTAs: email, phone, LinkedIn, and a resume PDF download
- Keyboard-accessible mobile navigation and a reduced-motion-aware reveal effect
- Works with JavaScript disabled; the script is progressive enhancement only

## Tech stack

HTML5, CSS3, and vanilla JavaScript. No framework, build step, bundler, or
runtime dependency. The only external request is the Google Fonts stylesheet
for Fraunces and Inter, both of which fall back to system fonts.

## Content source

Every fact on the page comes from `resume/vigneshwaran-resume.pdf`. No metrics,
project names, employers, logos, or links were invented. If the resume changes,
update `index.html` to match it rather than adding unsupported claims.

## Local preview

Open `index.html` directly, or serve the folder so that relative paths behave
exactly as they will in production:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Project structure

```text
resume-website/
├── index.html
├── style.css
├── script.js
├── README.md
├── .nojekyll
├── assets/
│   └── favicon.svg
└── resume/
    └── vigneshwaran-resume.pdf
```

## Deployment

The site is a static bundle at the repository root, so GitHub Pages can serve it
directly from a branch.

1. Push `index.html`, `style.css`, `script.js`, `assets/`, `resume/`,
   `README.md`, and `.nojekyll` to the repository root on `main`.
2. In GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select
   `main` and the `/ (root)` folder, then save.
4. Wait for the Pages build to finish and open the generated URL.
5. Test navigation, the LinkedIn link, the mail and phone links, and the PDF
   download on the live URL, and check developer tools for 404s.
6. Once the URL is stable, add the canonical link and Open Graph metadata to
   `index.html` and record the URL in the [Live site](#live-site) section above.

`.nojekyll` is present so GitHub Pages serves the files as-is rather than
running them through Jekyll.

## Accessibility and browser testing

- Skip link, visible `:focus-visible` outlines, and keyboard-operable navigation
- Mobile menu button exposes an accessible name plus `aria-expanded` and
  `aria-controls` state
- Semantic `header`, `main`, `section`, `article`, and `footer` elements with a
  single `h1` and a logical heading order
- Definition lists for the case-study details rather than visual-only layout
- Decorative SVG icons are hidden from assistive technology with `aria-hidden`
- `prefers-reduced-motion` disables the reveal animation and smooth scrolling
- Verified at 320px, 375px, 768px, 1024px, and wide desktop widths in current
  Chrome, Edge, Firefox, and Safari
- A print stylesheet hides navigation and CTAs for a clean paper copy

## Usage

Personal portfolio content. Reuse the layout and code freely; the resume
content and PDF belong to Vigneshwaran Ravichandran.
