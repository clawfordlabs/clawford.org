# clawford.org — Khorus Website

Static site for Stripe compliance. Hosted on GitHub Pages.

## Files

- `index.html` — Main landing page
- `terms.html` — Terms of Service
- `privacy.html` — Privacy Policy
- `refund.html` — Refund & Cancellation Policy
- `style.css` — Shared stylesheet
- `CNAME` — Custom domain config (clawford.org)

## Deploy to GitHub Pages

### 1. Create the repo

```bash
# On your machine (or Mac mini)
gh repo create lrettig/clawford.org --public
cd clawford-site
git init
git add .
git commit -m "Initial site — Stripe compliance"
git branch -M main
git remote add origin https://github.com/lrettig/clawford.org.git
git push -u origin main
```

### 2. Enable GitHub Pages

In the GitHub repo:
- Settings → Pages
- Source: **Deploy from a branch**
- Branch: `main`, folder: `/ (root)`
- Save

Your site will be live at `https://lrettig.github.io/clawford.org` within a minute.

### 3. Point your domain

In your DNS provider (wherever clawford.org is registered), add these records:

**A records** (for apex domain — clawford.org):
```
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
```

**CNAME record** (for www):
```
CNAME  www  lrettig.github.io
```

Then in GitHub repo Settings → Pages, set the custom domain to `clawford.org` and check "Enforce HTTPS".

DNS propagation takes up to 24h but usually a few minutes.

## Before Going Live — Fill These Placeholders

Search the HTML files for `[PLACEHOLDER` and replace:

1. **Address** — after setting up Anytime Mailbox
2. **Phone** — after setting up Google Voice

Files to update: `index.html`, `terms.html`, `privacy.html`, `refund.html`
