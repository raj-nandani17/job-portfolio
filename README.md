# Gotto Job — Frontend Job Portfolio Website

A responsive, multi-page job portal UI built with **HTML**, **CSS**, and a tiny bit of vanilla **JavaScript** (for the hamburger menu toggle hook). It includes a landing page, About, Contact, and Job Details pages — and styles for a (missing) Job Listings page you can add later.

> Live hosting is easiest with **GitHub Pages** — instructions below.

---

## ✨ Features
- Sticky header with logo + navigation — shared across pages (links to Home, Jobs, Contact, About). 【index.html】【about.html】【contact.html】【job-details.html】
- Full-bleed hero sections with overlay gradients and call-to-action blocks. 【styles.css】
- Search form UI component for job title & location (non-functional stub, ready to wire). 【index.html】【styles.css】
- Reusable job cards/badges/buttons and a "Similar Jobs" section on the details page. 【job-details.html】【job-details.css】
- Dedicated **About** and **Contact** pages with map embed & contact form. 【about.html】【contact.html】【contact.css】
- Mobile-responsive styles via media queries. 【styles.css】

> **Note:** Styles for **`job-listings.html`** are present, but the HTML file itself hasn’t been uploaded yet. You can create it later using the classes defined in `job-listings.css`. 【job-listings.css】

---

## 🗂️ Project Structure
```
/ (project root)
├── index.html              # Home / Landing page
├── about.html              # About page
├── contact.html            # Contact page with Google Map + form
├── job-details.html        # Individual job details + similar jobs
├── styles.css              # Global homepage styles
├── about.css               # About page styles
├── contact.css             # Contact page styles
├── job-details.css         # Job details page styles
└── job-listings.css        # Styles for (missing) job-listings.html
```
Referenced from the uploaded files. 【index.html】【about.html】【contact.html】【job-details.html】【styles.css】【about.css】【contact.css】【job-details.css】【job-listings.css】

---

## 📦 Tech & External Assets
- **HTML5**, **CSS3**, and vanilla **JS hooks** (no frameworks).
- **Fonts:** Google Fonts — *Sarabun* family imported in CSS. 【styles.css】
- **Icons:** Font Awesome via CDN. 【index.html】
- **Stock/Template images:** URLs point to Tooplate demo assets used for educational/demo purposes; replace with your own images before publishing. 【styles.css】【job-details.css】【about.css】

---

## 🚀 Getting Started (Run Locally)
1. **Download or clone** this repository.
2. Open `index.html` in your browser (double-click or use a local HTTP server).
   ```bash
   # optional: run a tiny local server
   # Python 3
   python -m http.server 5500
   # then visit http://localhost:5500/
   ```
3. Navigate between pages using the top navigation.

---

## 🧩 Pages Overview
- **Home (`index.html`)** — hero, search UI, categories, featured jobs, testimonials, CTA, footer. 【index.html】【styles.css】
- **About (`about.html`)** — intro, services/cards section (images + badges). 【about.html】【about.css】
- **Contact (`contact.html`)** — Google Maps embed, contact cards (office/website/phone/email), contact form, CTA, footer. 【contact.html】【contact.css】
- **Job Details (`job-details.html`)** — header + breadcrumb, job meta (location/date/salary/badges), description, company card, and **Similar Jobs** grid. 【job-details.html】【job-details.css】
- **Job Listings (missing)** — Use `job-listings.css` to style filters/search and list/grid of jobs. Create `job-listings.html` later. 【job-listings.css】

---

## 🛠️ How to Add `job-listings.html`
1. Create `job-listings.html`.
2. Link the stylesheet:
   ```html
   <link rel="stylesheet" href="job-listings.css">
   ```
3. Use the classes already defined in CSS, such as:
   - `.job-listeting` (hero header)
   - `.search-job`, `.hero-form`, `.inputs`, `.options`, `.form-option`
   - job card structure similar to the one in `job-details.html`'s "Similar Jobs" section. 【job-listings.css】【job-details.html】

---

## 🧭 Customization Notes
- **Branding:** Replace logo, title text, and footer info in each page’s `<header>`/footer blocks. 【index.html】【contact.html】【about.html】【job-details.html】
- **Images:** Swap external image URLs for local `assets/` images to avoid hotlinking and to speed up load. 【styles.css】【about.css】【job-details.css】
- **Icons:** Keep Font Awesome CDN or self-host the subset you need. 【index.html】
- **Mobile nav:** The hamburger icons are present; add a small JS to toggle `[data-visible]` on `.nav-links` for mobile menu (if not already wired). 【index.html】【styles.css】

Example toggle (optional):
```html
<script>
  const btn = document.querySelector('.hamburger');
  const list = document.querySelector('.nav-links');
  const bars = document.querySelector('.fa-bars');
  const closeI = document.querySelector('.fa-close');
  btn?.addEventListener('click', () => {
    const isOpen = list.getAttribute('data-visible') === 'true';
    list.setAttribute('data-visible', String(!isOpen));
    bars.setAttribute('data-visible', String(isOpen));
    closeI.setAttribute('data-visible', String(!isOpen));
  });
</script>
```

---

## 🌐 Deploy to GitHub Pages
### Option A — GitHub Website (no git commands)
1. Zip the project folder (optional but handy).
2. Create a new repo on GitHub (e.g., `job-portfolio`), **Public** or **Private**.
3. Click **Add file → Upload files** and drag your files in. Commit.
4. Go to **Settings → Pages**:
   - **Source:** Deploy from a branch
   - **Branch:** `main` → `/ (root)`
   - Save → GitHub will give you a Pages URL in a minute.
5. Visit the URL (something like `https://<username>.github.io/job-portfolio/`).

### Option B — Git (command line)
```bash
# inside your project folder
git init
git add .
git commit -m "Initial commit: Gotto Job frontend"
# create an empty repo on GitHub (no README)
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
# enable Pages as above (Settings -> Pages)
```

**Tip:** If your homepage doesn’t load as the root, ensure `index.html` is at the repository root (not nested). 【index.html】

---

## 🧪 Known Gaps / TODO
- Add **`job-listings.html`** to match navigation links and styles. 【index.html】【job-listings.css】
- Replace demo images and placeholder text (lorem ipsum) with real content. 【job-details.html】
- Optional: extract a shared header/footer into includes (if you later use a templating engine).

---


## 🙏 Credits
- Design inspiration and placeholder images: **Tooplate** demo assets referenced via absolute URLs in CSS/HTML. Replace before publishing commercially. 【styles.css】【about.css】【job-details.css】
- Icons: **Font Awesome** CDN. 【index.html】
- Fonts: **Google Fonts** (Sarabun). 【styles.css】

---

## 📬 Contact
Questions or want help wiring the listings page and mobile nav JS? Open an issue or reach out.
