# Raja Moiz Khalid — Portfolio

A single-page, animated 3D developer portfolio built with vanilla HTML, CSS, and JavaScript, using [Three.js](https://threejs.org/) for the interactive visuals. No build tools, no frameworks, no dependencies to install — just open it in a browser.

**Live demo:** _add your deployed link here once it's live (e.g. GitHub Pages URL)_

---

## Features

- **Animated hero section** with an ambient particle field and a floating, mouse-reactive photo cluster (orbiting rings + a hover-zoom photo)
- **3D wireframe text** in the About section that rotates and cycles smoothly through your programming languages
- **Sliding "pill" navigation** that follows your hovered/active section
- **Magnetic buttons** that ease toward the cursor on hover
- **Tilt-on-hover skill cards** and animated project list
- Fully responsive layout (desktop, tablet, mobile)
- Respects `prefers-reduced-motion` for accessibility
- All content driven by a single JavaScript data object — no HTML editing required to update your info

## Tech stack

- HTML5 / CSS3 (custom properties, CSS Grid & Flexbox)
- Vanilla JavaScript (ES6+, no framework)
- [Three.js r128](https://threejs.org/) for the 3D scenes (particles, wireframe text)
- [Google Fonts](https://fonts.google.com/): Fraunces, Inter, JetBrains Mono

## File structure

```
.
├── index.html      # entire site — markup, styles, and scripts in one file
├── profile.jpg     # profile photo used in the hero section
└── README.md
```

> ⚠️ `index.html` and `profile.jpg` must stay in the same folder — the page loads the photo using a relative path.

## Running it locally

No installation needed. Either:

- Double-click `index.html` to open it directly in your browser, **or**
- Serve it locally for the most reliable experience (some browsers restrict local file access for scripts):
  ```bash
  # Python 3
  python -m http.server 8000
  # then open http://localhost:8000
  ```

## Customizing your content

All of the site's text and data lives in one place: the `portfolioData` object near the top of the `<script>` section in `index.html`. Edit the values there and the page rebuilds itself automatically — no need to touch any HTML, CSS, or animation code.

```js
const portfolioData = {
  name: "...",
  role: "...",
  tagline: "...",
  email: "...",
  location: "...",
  resumeUrl: "...",
  photo: "profile.jpg",
  social: [ { label: "GitHub", url: "..." }, ... ],
  about: { bio: [...], facts: [...] },
  skills: [ { category: "...", items: [...] }, ... ],
  projects: [ { title: "...", year: "...", description: "...", tags: [...], liveUrl: "...", codeUrl: "..." }, ... ]
};
```

## Deploying to GitHub Pages

1. Create a new GitHub repository and push these files to it:
   ```bash
   git init
   git add index.html profile.jpg README.md
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, choose the `main` branch and `/ (root)` folder, then save.
4. GitHub will give you a live URL, typically:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```
5. Give it a minute or two after the first push, then visit the link.

## Credits

- Built with [Three.js](https://threejs.org/) (MIT License)
- Fonts via [Google Fonts](https://fonts.google.com/)

## Contact

- Email: rajamoiz608@gmail.com
- GitHub: [@RajaMoiz608](https://github.com/RajaMoiz608)
- LinkedIn: [moiz-khalid](https://www.linkedin.com/in/moiz-khalid-63644a337)
