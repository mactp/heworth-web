# Deploy Heworth Web (portfolio) + switch on the contact form

Live URL when done: **https://mactp.github.io/heworth-web/**

Two parts: (A) make the contact form work, (B) push the site live.
Do A first so the live site has a working form from day one.

> **Optional tidy-up:** the local folder is still called `tompyle-web` (I couldn't rename it
> from here — OneDrive locks it). Rename it to `heworth-web` in File Explorer if you like;
> the folder name doesn't affect the live URL either way.

---

## A. Turn on the contact form (Formspree — free)

The form is already wired up — it just needs *your* Formspree address.

1. Go to **https://formspree.io** and sign up (free) using **thom.pyle@gmail.com**.
2. Create a **New form** — call it "Heworth Web enquiries". Formspree gives you an
   endpoint like: `https://formspree.io/f/abcdwxyz`
3. Copy the part after `/f/` (e.g. `abcdwxyz`).
4. Open `index.html`, find this line (in the contact section near the bottom):
   ```html
   <form id="cform" action="https://formspree.io/f/YOUR_FORM_ID" method="POST" novalidate>
   ```
   Replace **YOUR_FORM_ID** with your real ID:
   ```html
   <form id="cform" action="https://formspree.io/f/abcdwxyz" method="POST" novalidate>
   ```
5. Save. Submissions now land in your Gmail.
   (On your first test submission, Formspree emails you a one-time "confirm this form" link.)

> The form already includes a hidden anti-spam honeypot, so you should get very little junk.

---

## B. Push the site live (GitHub Pages)

Run these in the VS Code terminal, inside the project folder.

```bash
git init -b main
git add -A
git commit -m "Heworth Web — portfolio site"
```

Create the repo on GitHub:
1. Go to **https://github.com/new**
2. Owner: **mactp** · Repository name: **heworth-web** · **Public**
3. **Don't** add a README/.gitignore/licence · click **Create repository**

Push it up:
```bash
git remote add origin https://github.com/mactp/heworth-web.git
git push -u origin main
```

Turn on Pages:
1. Repo → **Settings → Pages**
2. Source: **Deploy from a branch** · Branch: **main** · Folder: **/ (root)** · **Save**
3. Wait ~1–2 minutes.

Live at **https://mactp.github.io/heworth-web/**

---

## Making changes later
```bash
git add -A
git commit -m "what changed"
git push
```

---

### Optional next steps
- **Custom domain:** grab `heworthweb.co.uk` (check Namecheap) and point it at the site —
  same process as friendsofjsp.org.uk. Then a `hello@heworthweb.co.uk` email looks the part.
- **Tweak the copy:** the "Available for new projects" badge and the service area
  (York, Harrogate, Knaresborough) are easy to edit in `index.html`.
- Add more projects to the **Work** section as you build them.
