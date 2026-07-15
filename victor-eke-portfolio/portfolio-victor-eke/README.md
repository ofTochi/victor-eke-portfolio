# Victor Eke — Portfolio

A 5-page static site (Home, Work, Services, About, Contact) built from Stitch designs.
Plain HTML + Tailwind CDN — no build step required.

## Folder structure

```
portfolio-victor-eke/
├── index.html          Home
├── work.html            Selected work / case studies
├── services.html        Services offered
├── about.html            About / bio
├── contact.html          Contact form
└── README.md
```

## Run locally

Just open `index.html` in a browser, or serve it:

```
npx serve .
```

## Deploy to GitHub + Vercel

1. **Push to GitHub**
   ```bash
   cd portfolio-victor-eke
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/victor-eke-portfolio.git
   git push -u origin main
   ```

2. **Deploy on Vercel**
   - Go to vercel.com → **Add New Project** → Import the GitHub repo
   - Framework preset: **Other** (it's plain HTML, no build step)
   - Leave Build Command and Output Directory blank
   - Click **Deploy**

3. Vercel gives you a live `.vercel.app` URL immediately. Add a custom domain later under **Settings → Domains** if your friend has one.

## Known limitations / things to fix next

- All images currently point to Google's temporary AI-generated image URLs (`lh3.googleusercontent.com/aida-public/...`). These came from Stitch's design previews and **may expire or break** — swap them for real photos/assets before going live. Put real images in an `/assets` folder and update the `src`/`style="background-image:..."` references.
- Contact form doesn't actually send anywhere yet (`action="#"`) — hook it up to Formspree, Resend, or a simple serverless function when ready.
- Some decorative buttons (e.g. "Learn our process") still point to `#` — update once you know the real destinations.
