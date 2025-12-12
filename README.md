# taxiboatdriver.com

A collection of totally groundbreaking, never-seen-before Markdown templates for my simple website homepage – yet another way to display a title, some text, and a button. Prepare to bask in the glory of minimalism that screams, "I tried… kinda."

**Update:** It's no longer _that_ simple. Now it has custom layouts, SCSS variables, gradient accents, dark mode support, and a logo pill. So much for "minimal." But at least the content is still just Markdown.

---

## What is this?

This repository contains the content for **taxiboatdriver.com** – a tiny, text-driven, sarcasm-friendly homepage that started simple and gradually accumulated a custom Jekyll theme, CSS custom properties, and way too many design details for a site that's supposed to be minimal.

### It is

- a personal landing page for Serhii (`qizh`, `;,;`, `taxiboatdriver`);
- a place to experiment with tone, structure, and micro-copy;
- a low-friction way to ship changes by editing plain Markdown instead of fighting a giant CMS;
- a testbed for dark mode implementation, gradient styling, and other design experiments.

Jekyll was definitely harmed in the making of this site. Also SCSS. And my self-control regarding "keeping things simple."

---

## Technology Stack

Because "just Markdown" wasn't enough:

- **Jekyll** – Static site generator (GitHub Pages native)
- **jekyll-theme-architect** – Base theme (mostly overridden)
- **Custom Layout** – `_layouts/default.html` with gradient-styled header and logo pill
- **Custom SCSS** – `assets/css/style.scss` with CSS custom properties and dark mode support
- **Dark Mode** – Full `prefers-color-scheme` support with separate light/dark color palettes
- **SVG Logo** – Custom branding with `taxiboatdriver-icon.svg`
- **GitHub Pages** – Deployment with custom domain (`taxiboatdriver.com`)

So yeah, "simple" is relative.

---

## Features

### Dark Mode Support 🌙

Full automatic dark mode that responds to system preferences:
- CSS custom properties for dynamic color switching
- Optimized accent colors for each theme (darker teal in light, brighter in dark)
- WCAG-compliant contrast ratios
- Separate gradients for light and dark themes
- No JavaScript required (pure CSS via `@media (prefers-color-scheme: dark)`)

See [DARK_MODE_REVIEW.md](DARK_MODE_REVIEW.md) for the full review and technical details.

### Custom Design Elements

- **Gradient Header** – Horizontal gradient from lime-ish to teal (P3 color space)
- **Logo Pill** – Circular container with gradient border for the site icon
- **Section Tags** – Uppercase pills for section labels (Intro, Origin Story, Now, etc.)
- **Hover Effects** – Subtle interactions on sections and tags
- **Responsive Layout** – Mobile-first design that scales up to desktop

<details>
<summary>Live <mark><code>preview screenshots</code></mark> for <code>light</code> and <code>dark</code> color schemes</summary>

| Light | Dark |
|-------|------|
| ![Light mode preview](https://github.com/user-attachments/assets/2badc313-6142-45af-873d-da48601ae775) | _Set your system to dark mode and visit [taxiboatdriver.com](https://taxiboatdriver.com) to see the dark theme in action!_ 🌙 |

_The site automatically adapts to your system's color scheme preference using CSS `@media (prefers-color-scheme: dark)`._

</details>

---

<details>
  <summary>Additional Details</summary>

  ## Repository structure
  
  Current files and their purposes:
  
  ### Core Content
  - `index.md`  
    The main homepage content. This is where the actual "Hi, I'm Serhii and here's why this URL exists" text lives.
  
  ### Theme & Layout
  - `_config.yml`  
    Jekyll configuration with theme and site metadata.
  
  - `_layouts/default.html`  
    Custom Jekyll layout with gradient header, logo pill, and structured content sections.
  
  - `assets/css/style.scss`  
    Custom SCSS with CSS custom properties for theming, dark mode support, and all visual styling.
  
  ### Branding Assets
  - `taxiboatdriver-icon.svg`  
    Site logo (used in the header pill).
  
  - `taxiboatdriver_favicon.ico`  
    Favicon for browser tabs.
  
  ### Preview Files
  - `local-preview.html`  
    Standalone HTML file for previewing the site without Jekyll (automatic theme switching).
  
  - `local-preview-dark-forced.html`  
    Preview file with forced dark mode for testing.
  
  ### Documentation
  - `README.md`  
    You're reading it. Meta-text about the thing that serves more meta-text.
  
  - `DARK_MODE_REVIEW.md`  
    Comprehensive review of dark mode implementation with color analysis and accessibility testing.
  
  ### Deployment
  - `CNAME`  
    Custom domain configuration for GitHub Pages (`taxiboatdriver.com`).
  
  The repo is still _somewhat_ minimal, but it's evolved from "just Markdown" to a proper Jekyll site with custom theming.
  
  ---
  
  ## How to use this
  
  ### 1. Edit the homepage
  
  Open `index.md` and:
  - adjust sections,
  - rewrite text when your personality firmware gets updated,
  - add or remove blocks like "Languages I speak", "Projects", "Contact", etc.
  
  The layout and styling will automatically adapt to your content changes.
  
  ### 2. Preview locally
  
  You have multiple options:
  
  #### Option A: Full Jekyll Preview (recommended)
  
  ```bash
  # Install Jekyll if you haven't
  gem install bundler jekyll
  
  # Serve the site locally
  jekyll serve
  
  # Open http://localhost:4000
  ```
  
  This gives you the full Jekyll experience with live reloading.
  
  #### Option B: Standalone HTML Preview (quick)
  
  Just open `local-preview.html` in a browser. It includes all the CSS inline and will respond to your system's color scheme preference.
  
  For forced dark mode testing, use `local-preview-dark-forced.html`.
  
  #### Option C: Markdown Preview
  
  Use any Markdown preview in your editor (VSCode, Sublime, etc.) to see the content structure. You won't see the styling, but it's good for quick content edits.
  
  ### 3. Deploy
  
  The site is configured for GitHub Pages:
  - Push changes to the main branch
  - GitHub Pages automatically builds and deploys the Jekyll site
  - Changes appear at `taxiboatdriver.com` within a minute or two
  
  The `CNAME` file ensures the custom domain works correctly.
  
  ---
  
  ## Content philosophy
  
  Rough guidelines this repo tries to follow:
  
  ### Tone
  
  - `~70%` sarcasm and self-irony
  - `~30%` professionalism
    
  Enough seriousness to be taken seriously, enough jokes to admit we're all winging it.
    
  ### Honesty filter
    
  Public-safe personal details only:
  - where I'm from,
  - where I live now,
  - what I do,
  - what I enjoy,
  - some hobbies and interests.
    
  Deeper, more sensitive or over-personal topics live outside the public index or in private notes.
  
  ### Plain text first
    
  Everything starts as Markdown. No design tools required to update copy. The Jekyll layer is just presentation – content stays portable and format-agnostic.
  
  ---
  
  ## Roadmap
    
  ### Planned (or at least considered)
  
  - Translation to Russian.
  - Alternative intros for different moods (more serious / more chaotic).
  - A dedicated "Projects / Apps" section describing actual work.
  - A concise "Work with me" block with links and a less self-sabotaging pitch.
  - Optional subpages:
    - `/now` – what I'm currently focused on.
    - `/stack` – tools, devices, and tech I use.
    - `/lab` – experiments, drafts, and weird ideas that don't fit the front page.
  - More theme refinements (maybe a light/dark toggle button? or keep it automatic?)
  - Better mobile optimizations
    
  ### Whether all of this happens depends on
  - available time,
  - amount of procrastination,
  - and how much future-me regrets writing this roadmap.
  
  ---
  
  ## Contributing is not welcome
    
  This repository is primarily maintained by **future versions of myself**.
    
  ### External contributions policy
  - Pull requests from strangers:  
    appreciated in theory, suspicious in practice.
  - Issues:  
    feel free to open one if you spot a typo, a broken link, or an especially bad joke.
  - Forks:  
    if you somehow want to reuse this structure, go ahead. Just don't copy-paste the bio unless you also move to Koh Phangan for 11+ years.
  
  ---
  
  ## License
    
  Currently: "personal site, don't be weird about it" license.
    
  If I add a formal license later, it will show up here. Until then:
  - feel free to take inspiration from the structure and tone,
  - but avoid wholesale copy-pasting of personal text as-is.
</details>
