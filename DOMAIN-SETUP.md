# Custom domain + business email for Heworth Web

Goal: get the site onto **heworthweb.co.uk** (instead of mactp.github.io/heworth-web/)
and set up a **hello@heworthweb.co.uk** email.

You've done the domain part before for friendsofjsp.org.uk — same process.

---

## 1. Buy the domain  ⏱️ ~5 min
1. Go to **namecheap.com** and search **heworthweb.co.uk**.
   - If it's taken, good fallbacks: `heworth-web.co.uk`, `heworthwebstudio.co.uk`, `heworthweb.uk`.
2. Add it to basket and check out (~£6–9/year for .co.uk).
3. **Decline every upsell** — hosting, email, SSL, "PremiumDNS" etc. You don't need any of them
   (GitHub Pages gives free hosting + SSL). Just buy the domain itself.

---

## 2. Point the domain at GitHub Pages

### 2a. Tell GitHub the domain
1. Repo **mactp/heworth-web** → **Settings → Pages**
2. Under **Custom domain**, type `heworthweb.co.uk` → **Save**.
   (This automatically adds a `CNAME` file to your repo — don't delete it.)

### 2b. Add the DNS records at Namecheap
In Namecheap: **Domain List → Manage → Advanced DNS**. Delete any default
"parking" records, then add these:

| Type   | Host | Value                | TTL       |
|--------|------|----------------------|-----------|
| A      | @    | 185.199.108.153      | Automatic |
| A      | @    | 185.199.109.153      | Automatic |
| A      | @    | 185.199.110.153      | Automatic |
| A      | @    | 185.199.111.153      | Automatic |
| CNAME  | www  | mactp.github.io.     | Automatic |

(These are GitHub's official Pages IPs — identical to your JSP setup.)

### 2c. Wait, then turn on HTTPS
- DNS can take anywhere from 15 minutes to a few hours to propagate.
- Once GitHub shows the domain as verified (green tick in Settings → Pages),
  tick **Enforce HTTPS**.
- Done — your site is live at **https://heworthweb.co.uk** 🎉

---

## 3. Business email: hello@heworthweb.co.uk

Two options — pick one:

### Option A — Zoho Mail (recommended): a proper mailbox, free
A real inbox you can send *and* receive from, with webmail + a phone app. Free for 1 domain.
1. Sign up at **zoho.com/mail** → choose the **Forever Free Plan**.
2. Add your domain `heworthweb.co.uk` and verify it (Zoho gives you a TXT record to
   add in Namecheap → Advanced DNS).
3. Create the mailbox **hello@heworthweb.co.uk**.
4. Add the **MX records** Zoho gives you (in Namecheap → Advanced DNS):
   typically `mx.zoho.eu` (priority 10), `mx2.zoho.eu` (20), `mx3.zoho.eu` (50).
5. Add their SPF + DKIM records (Zoho walks you through it) so your email doesn't
   land in spam.

### Option B — Namecheap email forwarding: 2 minutes, receive-only
Simplest, but replies still come from your Gmail.
1. Namecheap → Domain List → Manage → **Redirect Email / Email Forwarding**.
2. Forward **hello@heworthweb.co.uk → thom.pyle@gmail.com**.
3. (Optional, fiddlier) set up Gmail "Send mail as" so replies show hello@.

> **My take:** go with **Zoho (Option A)** — for a business, being able to send *from*
> hello@heworthweb.co.uk looks far more professional, and free is free.

---

## 4. Once email is live — add it back to the site
When hello@heworthweb.co.uk works, tell me and I'll add it back to the contact section
(safe to show a business address; it was only your personal Gmail we wanted to hide).

---

### Quick order of play
1. Buy domain → 2. GitHub Pages custom domain → 3. Namecheap A + CNAME records →
4. Wait + Enforce HTTPS → 5. Set up Zoho email → 6. Tell me to add the address back.
