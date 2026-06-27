# Soowan Yang — Personal Homepage

Static academic homepage (plain HTML + CSS, no build step). Inspired by
[justin4ai.github.io](https://justin4ai.github.io/) and
[hchlhwang.github.io](https://hchlhwang.github.io/).

## 📂 Files
```
soowan-homepage/
├── index.html          # all content/sections
├── style.css           # styling (light/dark, responsive)
├── assets/
│   ├── profile.jpg     # ← put your selfie here (square works best)
│   └── CV_Soowan_Yang.pdf
└── README.md
```

## 1) Add your photo
Save your selfie as **`assets/profile.jpg`** (a square crop looks best — the
photo is shown in a circle). Until you add it, a placeholder is shown.

## 2) Preview locally
Just double-click `index.html`, or run a local server:
```bash
cd ~/Desktop/soowan-homepage
python3 -m http.server 8000   # then open http://localhost:8000
```

## 3) Publish on GitHub Pages
GitHub user/personal pages must live in a repo named **`<username>.github.io`**.

```bash
cd ~/Desktop/soowan-homepage
git init
git add .
git commit -m "Initial homepage"
git branch -M main
# create a repo named  <your-github-username>.github.io  on github.com first, then:
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```
Your site goes live at `https://<username>.github.io` within a minute or two.
(In repo **Settings → Pages**, confirm the source is `main` / root.)

## ✅ Already set up
- Profile photo, CV, Google Scholar link, email.
- Publications: each has **arXiv + Project Page + ▶ Video** links, and a
  **muted auto-looping video preview** (Hochul-style). The loops live in
  `assets/videos/` (`guidenav-loop.mp4`, `guidetwsi-loop.mp4`); clicking a
  preview opens the full YouTube video in a new tab.
  > Note: the auto-play loop only animates in a **real browser** (Chrome/Safari/
  > Firefox). Open `index.html` directly to see it move.
- **Gallery** section with two groups: Research (Fidelco guide-dog center) and
  Lab Life (UMass DARoS). Images live in `assets/research/` and `assets/lab/`.
  Click any photo to open it full-size (lightbox).

## ✏️ Optional things to tweak
- Add **Project Page** links to publications (search for `▶ Video` in `index.html`
  and add another `<a>` if you have a paper/PDF/arXiv link).
- Swap in more gallery photos: drop a JPG into `assets/research/` or `assets/lab/`
  and add a `<figure>` block in the `#gallery` section.
- Adjust the bio text at the top of `index.html` (`<section id="about">`).
