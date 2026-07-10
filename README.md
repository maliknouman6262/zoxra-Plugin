# Zoxra — Premium GPL Plugins & Themes Membership Website

A modern, dark-themed marketing website built for the **Zoxra** brand — a membership platform offering access to premium WordPress plugins and themes. Built with plain **HTML, CSS, and JavaScript** (no framework, no build step required).

> Client project — built and delivered by [Muhammad Nouman]. Not affiliated with WordPress.org, Automattic, or any plugin/theme authors mentioned.

---

## 🔗 Pages

| Page | File | Description |
|---|---|---|
| Home | `index.html` | Hero, feature highlights, plugin/theme services, "how it works" steps, WhatsApp CTA, full footer |
| Login | `login.html` | Email/password login form (front-end only) |
| Sign Up | `signup.html` | Full name, email, password, confirm password (front-end only) |

## 🗂 Project Structure

```
zoxra/
├── index.html      # Home page
├── login.html      # Login page
├── signup.html     # Sign up page
├── styles.css       # Shared design system (colors, type, layout, components)
├── script.js         # Shared JS (mobile nav toggle, demo form handling)
└── README.md
```

## 🎨 Design System

- **Font pairing:** Fraunces (display/serif) + Inter (body/UI), loaded via Google Fonts
- **Palette:** Near-black background with a brass/gold accent, WhatsApp green used only for WhatsApp CTAs
- **Layout:** Fully responsive — desktop, tablet, and mobile breakpoints included
- **Accessibility:** Visible focus states on all interactive elements, `prefers-reduced-motion` respected

## ⚙️ Running Locally

No build tools or dependencies are required. Any static file server works:

```bash
# Option 1 — Python
python3 -m http.server 8080

# Option 2 — VS Code
# Right-click index.html → "Open with Live Server"
```

Then open `http://localhost:8080` in your browser.

## 🧾 Important Notes for the Client

- The **Login** and **Sign Up** forms are front-end only — they do not currently connect to a database or authentication service. Submitting a form shows a confirmation message but does not create real accounts. Connect them to your backend/auth provider (e.g., Firebase, Supabase, custom API) before going live if real accounts are needed.
- Update the **WhatsApp number** (`+44 741 7457079`) in `index.html`, `login.html`, and `signup.html` if it changes — search for `wa.me/447417457079` to find every instance.
- Replace the footer's **Terms of Service / Privacy Policy / GPL Disclosure** links (`#` placeholders) with real pages before launch.
- Update `© 2026 Zoxra` in the footer if needed for future years.

---

## 🚀 Deploying

### Upload to GitHub

```bash
cd zoxra
git init
git add .
git commit -m "Initial commit — Zoxra website"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

### Deploy to Vercel

**Option A — Vercel Dashboard (no CLI needed)**
1. Push the project to GitHub (steps above).
2. Go to [vercel.com/new](https://vercel.com/new) and import the GitHub repository.
3. Framework Preset: choose **Other** (this is a static site, no build step needed).
4. Leave **Build Command** and **Output Directory** blank.
5. Click **Deploy** — Vercel will serve `index.html`, `login.html`, and `signup.html` directly.

**Option B — Vercel CLI**
```bash
npm i -g vercel
cd zoxra
vercel
```
Follow the prompts (set up and deploy → link to a new project). Vercel will detect it as a static site automatically.

Once deployed, your live URLs will look like:
- `https://your-project.vercel.app/` → Home
- `https://your-project.vercel.app/login.html` → Login
- `https://your-project.vercel.app/signup.html` → Sign Up

---

## 📄 License

This codebase is delivered to the client as a custom project. All rights to the final design and code belong to the client per the project agreement. Plugin/theme names mentioned (e.g., Elementor Pro, Astra Pro, Rank Math) are trademarks of their respective owners and are referenced for illustrative purposes only.
