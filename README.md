# Spencer Levine — Portfolio Website - Claude created ts, thank you anthropic!!

Personal engineering portfolio site. Built with plain HTML/CSS/JS — no frameworks, no build step.

## 🚀 Live Site
Hosted on GitHub Pages: `https://YOUR-USERNAME.github.io/spencer-portfolio`

---

## 📁 Folder Structure

```
spencer-portfolio/
│
├── index.html                  ← The entire website (edit this)
│
├── resume/
│   └── Spencer_Levine_Resume.pdf   ← Drop your resume PDF here
│
├── images/
│   ├── hero-photo.jpg              ← Your circular headshot (home page)
│   ├── about-photo.jpg             ← Hard hat photo (about page)
│   │
│   ├── gripper/
│   │   ├── thumb.jpg               ← Portfolio grid thumbnail
│   │   ├── 1.jpg                   ← Detail page gallery image 1
│   │   ├── 2.jpg
│   │   ├── 3.jpg
│   │   ├── 4.jpg
│   │   ├── 5.jpg
│   │   └── 6.jpg
│   │
│   ├── swerve/    (same structure: thumb + 1–6)
│   ├── arm/
│   ├── ftc/
│   ├── stock/
│   ├── housing/
│   ├── hammer/
│   ├── dog/
│   ├── animation/
│   └── gumball/
│
└── videos/
    ├── gripper/
    │   └── preview.mp4             ← Short muted hover-preview clip (5–15s)
    ├── swerve/
    ├── arm/
    ├── ftc/
    ├── stock/
    ├── housing/
    ├── hammer/
    ├── dog/
    ├── animation/
    └── gumball/
```

---

## 🖼️ How to Add Images

In `index.html`, find placeholders like `[GRIPPER_1.jpg]` and replace the whole `<div class="proj-gallery-ph">` block with:

```html
<img class="proj-gallery-img" src="images/gripper/1.jpg" alt="Robotic gripper">
```

For the portfolio grid thumbnail, find `[GRIPPER_THUMB.jpg]` and replace the `<div class="project-thumb-ph">` block with:

```html
<img class="project-thumb" src="images/gripper/thumb.jpg" alt="Robotic gripper">
```

---

## 🎬 How to Add YouTube Videos (Full Video on Project Pages)

1. Upload your video to YouTube as **Unlisted**
2. Copy the video ID from the URL (the part after `v=`, e.g. `dQw4w9WgXcQ`)
3. In `index.html`, find the project in the `PROJECTS` array in the `<script>` tag
4. The video placeholder div will be replaced automatically — just swap the embed in the rendered `proj-video-ph` divs, or update the JS to render iframes directly:

```html
<iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" allowfullscreen></iframe>
```

---

## 🎥 How to Add Hover Preview Videos

Each project card in the portfolio grid can show a short muted video on hover.

1. Put a short clip (5–15 seconds, MP4) in `videos/gripper/preview.mp4`
2. In `index.html`, find the project card and replace the thumbnail with:

```html
<div class="project-thumb-wrap">
  <img class="project-thumb" src="images/gripper/thumb.jpg" alt="Gripper">
  <video class="project-thumb-video" src="videos/gripper/preview.mp4" muted loop playsinline></video>
</div>
```

The CSS and JS for hover-play is already built into the site.

---

## 📄 How to Update Your Resume PDF

1. Export your latest resume as a PDF
2. Name it exactly: `Spencer_Levine_Resume.pdf`
3. Drop it in the `resume/` folder
4. The download button on the Resume page will automatically link to it

---

## 🌐 How to Deploy on GitHub Pages

1. Create a new repo on GitHub: `github.com/new`
   - Name it `spencer-portfolio` (or anything)
   - Set to **Public**
2. Upload all files (drag and drop on GitHub, or use Git)
3. Go to **Settings → Pages**
4. Under "Source", select **Deploy from branch → main → / (root)**
5. Hit Save — your site will be live in ~60 seconds at:
   `https://YOUR-USERNAME.github.io/spencer-portfolio`

### Connecting a Custom Domain (~$12/year)
1. Buy a domain on [Namecheap](https://namecheap.com) or [Porkbun](https://porkbun.com)
2. In GitHub Pages settings, enter your domain under "Custom domain"
3. In your domain registrar, add a CNAME record:
   - **Host:** `www`
   - **Value:** `YOUR-USERNAME.github.io`
4. Done — takes 10–30 min to propagate

---

## ✏️ Editing the Site

**On GitHub (easy):** Click `index.html` → pencil icon → edit → commit

**In VS Code (browser, no install):** Press `.` on any GitHub repo page to open VS Code in the browser

**Locally:** Download the repo, open `index.html` in Chrome to preview, edit in any text editor
