# lhm6199.github.io

Personal academic website built with static HTML and CSS.

## File Structure

- `index.html`: Main profile page. Edit this file for most content changes.
- `style.css`: Shared visual style and responsive layout.
- `photo.png`: Profile image used in the about section.
- `post-llm-execution.html`: Example standalone note page linked from publications.

## How to Edit Sections

### Navigation

Edit the list inside `<ul class="nav-links">` in `index.html`.

Add a new section link like this:

```html
<li><a href="#news">news</a></li>
```

The `href` value must match the target section id, for example:

```html
<section class="content-section" id="news">
```

### About

Edit the about section in `index.html`:

```html
<section class="profile-section" id="about">
```

Change your name:

```html
<h1>Hyunmin Lee</h1>
```

Change your role:

```html
<p class="role">Software Engineering Student @ Sungkyunkwan University</p>
```

Change your email:

```html
<p class="email"><a href="mailto:lhm6199@gmail.com">lhm6199@gmail.com</a></p>
```

Add or remove external links inside:

```html
<div class="profile-links" aria-label="External links">
```

Example:

```html
<a href="https://github.com/lhm6199" target="_blank" rel="noreferrer">GitHub</a>
```

### Publications

Edit this section in `index.html`:

```html
<section class="content-section" id="publications">
```

Publications are split into groups:

```html
<div class="publication-group">
    <h3>Selected Publications</h3>
    <ol class="numbered-publications">
```

Add a publication by copying one `<li>...</li>` block inside the target `<ol>`.

Template:

```html
<li>
    <span class="pub-tag">DAC 2026</span>
    <p>Author Names; <a href="https://example.com" target="_blank" rel="noreferrer">Paper Title</a>. In Venue Name, 2026.</p>
</li>
```

For the second publication group, use:

```html
<ol class="numbered-publications" start="6">
```

Change the `start` value so the numbering continues from the previous group.

### Education

Edit this section in `index.html`:

```html
<section class="content-section" id="education">
```

Add an education item by copying this template inside `<div class="cv-list">`:

```html
<article class="cv-item">
    <span class="cv-date">2023.03 - Present</span>
    <div>
        <h3>Degree Name</h3>
        <p>University Name.</p>
    </div>
</article>
```

### Experience

Edit this section in `index.html`:

```html
<section class="content-section" id="experience">
```

Add an experience item by copying this template inside `<div class="cv-list">`:

```html
<article class="cv-item">
    <span class="cv-date">2025.07 - Present</span>
    <div>
        <h3>Position Title</h3>
        <p>Lab, company, or organization name.</p>
    </div>
</article>
```

### Honors and Awards

Edit this section in `index.html`:

```html
<section class="content-section" id="honors">
```

Add an award inside `<ul class="award-list">`:

```html
<li><span>2025.09</span><p>Award Name, Organization.</p></li>
```

### Legacy Activity Format

The current homepage uses `Education`, `Experience`, and `Honors and Awards` instead of a single activity section.
If you want to add a general activity section again, use this structure:

Template:

```html
<section class="content-section" id="activities">
    <div class="section-heading">
        <h2>activities</h2>
    </div>
    <div class="cv-list">
        <article class="cv-item">
            <span class="cv-date">Mar 2026 - Present</span>
            <div>
                <h3>Activity Name</h3>
                <p>Short description of what you did.</p>
            </div>
        </article>
    </div>
</section>
```

### News

Edit this section in `index.html`:

```html
<section class="content-section" id="news">
```

Add a news item inside:

```html
<ul class="news-list">
```

Template:

```html
<li>
    <time datetime="2026-06-21">Jun 21, 2026</time>
    <span>News text goes here.</span>
</li>
```

Use `datetime="YYYY-MM-DD"` for machine-readable dates.

### Profile Photo

Replace `photo.png` with another image using the same filename, or update this line in `index.html`:

```html
<img src="photo.png" alt="Portrait of Hyunmin Lee">
```

The image is displayed as a circle by `style.css`.

### Light and Dark Mode

The site supports light and dark mode through CSS variables in `style.css`.

Light mode values are defined in:

```css
:root {
```

Dark mode values are defined in:

```css
[data-theme="dark"] {
```

To change the background or text colors, edit variables such as:

```css
--bg: #ffffff;
--text: #202124;
--muted: #5f6368;
--line: #e5e7eb;
```

The theme toggle button is in the navigation area of each HTML page:

```html
<button class="theme-toggle" type="button">dark</button>
```

If you add a new HTML page, copy the same theme button and the two theme scripts from an existing page so the saved mode works consistently.

## Local Preview

Open `index.html` directly in a browser, or run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/
```
