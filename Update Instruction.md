# How to Update Your Personal Website

You don't need any coding skills to update your site.
Everything is done directly on the GitHub website.

---

## How to Open and Edit Your File

1. Go to [github.com](https://github.com) and log in
2. Click on your repository (named `yourusername.github.io`)
3. Click on `index.html`
4. Click the **pencil icon** (top right of the file view) to edit
5. Make your changes (see sections below)
6. Click the green **Commit changes** button when done
7. Your site updates live within **1–2 minutes**

---

## Add a New Blog Post

Find this section in the file (search for `blog-list`):

```html
<div class="blog-list">
  <a href="#" class="blog-item">
    <span class="blog-date">Apr 2025</span>
    <span class="blog-title">Why most financial models fail...</span>
    <span class="blog-arrow">→</span>
  </a>
  ...
```

To add a new post, copy one `<a>` block and paste it at the **top** of the list:

```html
<a href="#" class="blog-item">
  <span class="blog-date">Apr 2026</span>
  <span class="blog-title">Your new blog post title here</span>
  <span class="blog-arrow">→</span>
</a>
```

**What to change:**
- `Apr 2026` → the month and year of your post
- `Your new blog post title here` → your actual title
- `href="#"` → if you have a link to your post, replace `#` with the URL

---

## Update Work Experience

Find this section (search for `timeline`):

```html
<div class="timeline-item">
  <p class="timeline-date">2022 — Present</p>
  <p class="timeline-role">Senior Financial Analyst</p>
  <p class="timeline-company">Company Name · Full-time</p>
  <p class="timeline-desc">
    Led FP&A for a $500M business unit...
  </p>
</div>
```

To **add a new job**, copy the whole `<div class="timeline-item">...</div>` block and paste it at the **top** of the timeline. Then update:

| Field | What to change |
|---|---|
| `timeline-date` | e.g. `2024 — Present` |
| `timeline-role` | Your job title |
| `timeline-company` | Company name and type (Full-time / Contract) |
| `timeline-desc` | 2–3 sentences about what you did |

To **edit an existing job**, just find it and change the text directly.

---

## Add a New Project

Find the section (search for `projects-grid`):

```html
<div class="project-card">
  <span class="project-tag">Financial Modelling</span>
  <p class="project-title">Three-Statement LBO Model</p>
  <p class="project-desc">A fully integrated LBO model...</p>
  <a href="#" class="project-link">View model →</a>
</div>
```

Copy one card block and paste it inside `projects-grid`. Then update:

| Field | What to change |
|---|---|
| `project-tag` | Category (e.g. Research, Dashboard, Strategy) |
| `project-title` | Name of your project |
| `project-desc` | Short description (2–3 sentences) |
| `href="#"` | Link to your project if you have one |

---

## Update Your About / Bio

Find this section (search for `Hi — I'm Alex`):

```html
<p>
  Hi — I'm Alex. I'm a finance professional based in [Your City] with
  [X] years of experience...
</p>
```

Just rewrite the text between the `<p>` and `</p>` tags.

---

## Update the Stats (Numbers)

Find the four stat cards (search for `stat-number`):

```html
<p class="stat-number">8+</p>
<p class="stat-label">Years in finance</p>
```

Change the number and label text to match your actual figures.

---

## Update Your Name

Search for `Alex Morgan` in the file and replace all instances with your real name.
There are 3 places: the browser tab title, the nav logo, and the footer.

---

## Update Contact Details

Search for these placeholders and replace them:

| Placeholder | Replace with |
|---|---|
| `hello@yourname.com` | Your email address |
| `linkedin.com/in/yourname` | Your LinkedIn URL |
| `github.com/yourname` | Your GitHub URL |

---

## Add Your Photo

Find this block:

```html
<div class="photo-frame"></div>
```

Replace it with:

```html
<img src="photo.jpg" alt="Your Name"
  style="width:340px; height:400px; object-fit:cover; border-radius:4px;" />
```

Then upload your photo file named `photo.jpg` to your GitHub repository
alongside `index.html` (use **Add file → Upload files**).

---

## Quick Checklist When You Update

- [ ] Changed the text correctly (don't delete any `<` or `>` symbols)
- [ ] Clicked **Commit changes** at the bottom
- [ ] Waited 1–2 minutes then refreshed your site to check

> **Tip:** If something looks broken, click on `index.html` in GitHub,
> then click **History** to go back to a previous version.
