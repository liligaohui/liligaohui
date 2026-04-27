# Personal Website — Developer Guide

Everything you need to understand how the site is built,
how to open it locally, and how it is structured.

---

## What This Website Is

This is a **single-file static website** — the entire site lives in one file: `index.html`.

- No frameworks (no React, no WordPress, no plugins)
- No server needed
- No installation needed
- Works in any browser, on any computer
- Free to host on GitHub Pages forever

---

## Files in This Project

```
yourusername.github.io/
│
├── index.html        ← The entire website (HTML + CSS + JS all in one)
├── photo.jpg         ← Your profile photo (add this yourself)
│
├── HOW_TO_UPDATE.md  ← Guide for updating content (blog, experience, projects)
├── HOW_TO_DEVELOP.md ← This file
└── GITHUB_SETUP.md   ← Guide for deploying to GitHub Pages
```

---

## How to Open the Site Locally (No Internet Needed)

You don't need to upload to GitHub every time you make a change.
You can preview it on your own computer first:

**Step 1 — Download the file**
- Go to your GitHub repo
- Click `index.html`
- Click the **Download raw file** button (or right-click → Save As)
- Save it somewhere easy to find, like your Desktop

**Step 2 — Open it in a browser**
- Find `index.html` on your computer
- Double-click it
- It opens in your browser — this is your website!

**Step 3 — Edit and preview**
- Open `index.html` in a text editor (see below)
- Make a change and save the file
- Go back to the browser and press **F5** (or Cmd+R on Mac) to refresh
- You'll see your changes instantly

> You can do all your editing and previewing locally this way.
> Only upload to GitHub when you're happy with the result.

---

## Recommended Free Text Editors

You need a text editor to edit `index.html`. Do NOT use Word or Notepad —
they can corrupt the file. Use one of these instead:

| Editor | Download | Best for |
|---|---|---|
| **VS Code** | [code.visualstudio.com](https://code.visualstudio.com) | Best overall, free |
| **Notepad++** | [notepad-plus-plus.org](https://notepad-plus-plus.org) | Windows, lightweight |
| **TextEdit** | Built into Mac | Mac, simple edits |

**VS Code is recommended** — it colour-codes HTML so it's easy to read,
and underlines mistakes automatically.

---

## How the File is Structured

`index.html` is divided into three parts:

```
index.html
│
├── <head>          Invisible settings: page title, fonts, styles (CSS)
│
├── <body>          Everything visible on the page
│   ├── <nav>           Top navigation bar
│   ├── #hero           Name, tagline, photo, buttons
│   ├── #about          Bio + stat cards
│   ├── #experience     Timeline of jobs
│   ├── #projects       Project cards grid
│   ├── #blog           Blog post list
│   ├── #contact        Contact form + social links
│   └── <footer>        Copyright line
│
└── <script>        Small animations (runs at the bottom)
```

Each section is wrapped in a tag like:
```html
<section id="about">
  ... all the about content here ...
</section>
```

To find any section quickly, use **Ctrl+F** (or Cmd+F on Mac) to search
for the section ID, e.g. search `id="blog"` to jump straight to the blog section.

---

## How the Design Works (CSS)

All styling is inside the `<style>` block near the top of the file.
The design uses **CSS variables** — think of them as named colours and settings
you define once and reuse everywhere:

```css
:root {
  --cream:   #FAF8F4;   /* background colour */
  --ink:     #1A1814;   /* main text colour */
  --accent:  #2C5F4A;   /* green used for highlights */
  --serif:   'DM Serif Display', serif;   /* heading font */
  --sans:    'DM Sans', sans-serif;       /* body font */
}
```

To change the accent colour across the whole site, just change `--accent` here.
You don't need to find and change every individual element.

**Fonts** are loaded from Google Fonts (requires internet). They are:
- **DM Serif Display** — used for all headings (elegant, editorial)
- **DM Sans** — used for all body text (clean, minimal)

---

## How the Animations Work

The site has two types of animation:

**1. Hero fade-in** — the name, tagline and photo fade up on page load.
These use CSS classes like `fade-up`, `delay-1`, `delay-2` etc.
Each adds a slightly longer delay so elements appear one by one.

**2. Scroll reveal** — sections fade in as you scroll down.
This uses a small JavaScript block at the bottom of the file
called `IntersectionObserver` — it watches for elements entering
the screen and makes them visible.

You don't need to touch either of these. They just work.

---

## How the Contact Form Works

The form currently shows a browser alert when submitted.
To make it send you real emails, connect it to **Formspree** (free):

1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form — you'll get a URL like `https://formspree.io/f/xxxxxxxx`
3. In `index.html`, find the `<form>` tag and change it to:

```html
<form action="https://formspree.io/f/YOUR_ID" method="POST">
```

4. Remove `onsubmit="handleSubmit(event)"` from the same line
5. Save and upload — the form now sends emails to you directly

---

## How to Add a Completely New Section

If you want to add a section that doesn't exist yet (e.g. Certifications, Testimonials):

1. Copy an existing section block, for example the `#about` section
2. Paste it after the last `</section>` and before `<hr class="divider">`
3. Change the `id="about"` to your new section name, e.g. `id="certifications"`
4. Add a link to it in the nav:

```html
<li><a href="#certifications">Certifications</a></li>
```

5. Update the content inside

---

## How to Change the Colour Theme

All colours are defined at the top of the `<style>` block:

```css
:root {
  --cream:        #FAF8F4;   /* page background */
  --ink:          #1A1814;   /* main text */
  --ink-soft:     #5A5650;   /* secondary text */
  --ink-muted:    #9A9590;   /* placeholder / hint text */
  --accent:       #2C5F4A;   /* green highlight colour */
  --accent-light: #E8F0EC;   /* light green for tags/badges */
  --border:       #E4E0D8;   /* lines and borders */
}
```

To change the theme, just swap out these hex colour values.
For example, to use a navy blue accent instead of green:
- Change `--accent` to `#1B3A6B`
- Change `--accent-light` to `#E3EAF4`

Use [coolors.co](https://coolors.co) to find colour combinations.

---

## Uploading Changes to GitHub

Once you've edited and previewed locally:

1. Go to your GitHub repository
2. Click on `index.html`
3. Click the **pencil icon** to edit
4. Paste in your updated content (or use the Upload option to replace the file)
5. Click **Commit changes**
6. Site updates in ~1 minute

---

## Summary

| Task | Where |
|---|---|
| Preview site | Double-click `index.html` in your browser |
| Edit content | Open `index.html` in VS Code or a text editor |
| Change colours / fonts | Edit the `:root { }` block near the top |
| Add a section | Copy an existing `<section>` block |
| Make form send emails | Connect to Formspree |
| Publish updates | Upload `index.html` to GitHub and commit |
