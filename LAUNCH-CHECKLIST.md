# This week: get the foundations live ✅

The goal: a working portfolio link + a working contact form. That's the whole job this week.
Detailed commands are in `DEPLOY.md` — this is the tick-list version.

---

## Already done ✓
- [x] Heworth Joinery demo built **and live** → https://mactp.github.io/heworth-joinery-demo/
- [x] Heworth Web portfolio site built
- [x] Contact form wired up (just needs your Formspree ID — step 1 below)

---

## 1. Switch on the contact form  ⏱️ ~5 min
- [ ] Go to **formspree.io** and sign up (free) with **thom.pyle@gmail.com**
- [ ] Create a new form, name it "Heworth Web enquiries"
- [ ] Copy your form ID (the bit after `/f/`, e.g. `abcdwxyz`)
- [ ] In `index.html`, find `action="https://formspree.io/f/YOUR_FORM_ID"` and replace `YOUR_FORM_ID` with yours
- [ ] Save the file

## 2. Deploy the portfolio  ⏱️ ~10 min
- [ ] Open the portfolio folder in **VS Code**
- [ ] In the terminal: `git init -b main` → `git add -A` → `git commit -m "Heworth Web portfolio"`
- [ ] Create the repo at **github.com/new** → owner **mactp**, name **heworth-web**, Public, no README
- [ ] `git remote add origin https://github.com/mactp/heworth-web.git` → `git push -u origin main`
- [ ] On GitHub: **Settings → Pages → Deploy from branch → main → / (root) → Save**
- [ ] Wait ~2 min, then open **https://mactp.github.io/heworth-web/**

## 3. Test that it actually works  ⏱️ ~5 min
- [ ] Open the **portfolio on your phone** — check the hero, buttons and layout look right
- [ ] Open the **Heworth demo on your phone** — same quick check
- [ ] **Submit the contact form** as a test → confirm Formspree's one-time verification email → check the test message lands in your Gmail
- [ ] Click **every nav link** and both **project links** (JSP + Heworth demo) — make sure they all open

## 4. Quick polish pass  ⏱️ ~5 min
- [ ] Read the page copy once for typos
- [ ] Is the **"Available for new projects"** badge true right now? (Remove it if not)
- [ ] Is the service area right? (York · Harrogate · Knaresborough)
- [ ] Does the JSP card's **"WIP"** note still feel accurate?

---

## ✅ When all four are ticked, you have:
- A live portfolio at **mactp.github.io/heworth-web/**
- A contact form that lands enquiries in your inbox
- A live demo site to show prospects

**Then — and only then — the next step is outreach** (warm list + the free-mockup pitch).
Building is done; getting in front of people is what turns this into money.
