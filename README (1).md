# HTML CV Template — One Page, Print-Ready

A clean, responsive CV page built with pure HTML and CSS. No frameworks, no dependencies. Works in the browser, looks great on mobile, and prints as a professional one-page PDF.

**[Live example →](https://natalialeaiart.github.io/cv)**

---

## What's included

- Responsive layout (desktop + mobile)
- Print-ready styling — one page A4, no browser headers/footers
- Download PDF button (links to your pre-saved PDF file)
- Click-to-copy email
- Sections: Hero with photo, Skills, Experience, Education, Languages
- Optional "about me" link block at the bottom (hidden in print)

---

## How to use

### 1. Fork or download

Click **Use this template** (or download the ZIP) and create your own repository.

Your repo should contain:
```
index.html
unnamed.png      ← your photo
cv.pdf           ← your PDF (see step 4)
README.md
```

### 2. Edit `index.html`

Open the file in any text editor. Find and replace the following:

**Your name and title**
```html
<h1>Nataļja Levaškoviča</h1>
<div class="subtitle">HR Business Partner</div>
```

**Your photo**
```html
<img class="hero-photo" src="unnamed.png" alt="Your Name" />
```
Replace `unnamed.png` with your photo file. Keep it in the same folder.

**Your contacts**
```html
<span ... onclick="copyEmail()">natalja.levaskovica@inbox.lv</span>
<a ...>+371 26 106 616</a>
<a ...>linkedin.com/in/yourprofile</a>
```
Also update the email inside the `copyEmail()` function in the script at the bottom:
```js
navigator.clipboard.writeText('your@email.com')
```

**Your bio**
```html
<p class="bio">HR professional with 15+ years...</p>
```

**Skills** — just edit the text inside `<span class="skill-tag">` elements.
Tags with class `accent` are highlighted in burgundy — use these for your strongest skills.

**Experience** — copy/paste `.exp-item` blocks as needed:
```html
<div class="exp-item">
  <div class="exp-header">
    <div class="exp-title">Your Job Title</div>
    <div class="exp-period">Jan 2020 — Dec 2023</div>
  </div>
  <div class="exp-company">Company Name · City, Country</div>
  <ul class="exp-desc">
    <li>What you did and what impact it had.</li>
    <li>Another achievement or responsibility.</li>
  </ul>
</div>
```

**Languages**
```html
<div class="lang-item">
  <span class="lang-name">English</span>
  <span class="lang-level native">Native</span>
</div>
```
Available level classes: `native` · `professional` · `working`

**Education**
```html
<div class="edu-degree">Your Degree</div>
<div class="edu-school">University Name · Field of Study</div>
<div class="edu-year">2004 – 2009</div>
```

**Optional footer link** — if you have a portfolio or another page to link to, update this block. If you don't need it, delete the entire `<div class="ai-footer">` section.

---

### 3. Change the color scheme (optional)

All colors are defined as CSS variables at the top of the file:

```css
:root {
  --accent:       #7B2D42;   /* main color — burgundy */
  --accent-hover: #9E3A54;
  --accent-light: rgba(123, 45, 66, 0.12);
  --bg-card:      #F7F5F3;   /* page background */
  --text-dark:    #1C1C1C;
  --text-mid:     #444444;
}
```

Change `--accent` to any color to instantly restyle the whole page.
Examples:
- Navy: `#1B3A6B`
- Forest green: `#2D5A3D`
- Slate: `#3D4E6B`

---

### 4. Create your PDF

1. Open `index.html` in **Chrome** or **Edge**
2. Press `Ctrl+P` (or `Cmd+P` on Mac)
3. Set destination: **Save as PDF**
4. Open **More settings**:
   - ✅ Paper size: A4
   - ✅ Margins: Default
   - ❌ Headers and footers: **off** ← this removes the date and URL
5. Save the file as `cv.pdf` and put it in the same folder as `index.html`

The **Download PDF** button will automatically serve this file with the name you set in the `download` attribute:
```html
<a href="cv.pdf" download="Your Name — Job Title.pdf">
```
Change the `download` value to whatever you want the file to be called when downloaded.

---

### 5. Publish with GitHub Pages

1. Push your files to a GitHub repository
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)`
4. Your CV will be live at `https://yourusername.github.io/cv`

---

## File structure

```
cv/
├── index.html        # the CV page
├── unnamed.png       # your photo
├── cv.pdf            # downloadable PDF version
└── README.md         # this file
```

---

## Tips

- **Photo**: portrait orientation works best. The template applies grayscale automatically — color photo is fine.
- **One page**: if your CV is spilling onto a second page when printing, shorten your bullet points or reduce the number of experience entries.
- **Mobile**: the layout stacks the photo above the text on small screens automatically.
- **Fonts**: the template uses [Raleway](https://fonts.google.com/specimen/Raleway) loaded from Google Fonts. Requires internet connection to display correctly.

---

*Template by [Nataļja Levaškoviča](https://natalialeaiart.github.io/cv) · Made with HTML, CSS, and a little help from AI*
