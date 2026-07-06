# Deploying mlbroe.com → GitHub Pages

This repo is a static site. Deploy it the same way as stagetwopartners.io.

---

## Step 1 — Create a GitHub repo

1. Go to **github.com** → **+** (top right) → **New repository**
2. Name it e.g. `mlbroe-website`
3. Set it to **Public** (required for free GitHub Pages)
4. Don't add a README — leave it empty
5. Click **Create repository**

---

## Step 2 — Push this project

From this folder:

```bash
git remote add origin https://github.com/YOUR-USERNAME/mlbroe-website.git
git branch -M main
git push -u origin main
```

(Files are already committed locally.) Alternatively, drag the files into the empty
repo on github.com — but include the whole `images/` folder and the `CNAME` file.

---

## Step 3 — Enable GitHub Pages

1. Repo → **Settings** → **Pages**
2. **Source** → **Deploy from a branch**
3. Branch: **main** | Folder: **/ (root)** → **Save**

GitHub shows: *"Your site is live at https://YOUR-USERNAME.github.io/mlbroe-website"*

---

## Step 4 — Custom domain

Still on the Pages settings page:

1. **Custom domain** → type `mlbroe.com` → **Save**
2. Check **Enforce HTTPS** (appears after a few minutes)

The `CNAME` file in this repo already contains `mlbroe.com`.

---

## Step 5 — DNS at your registrar

Point the domain at GitHub Pages. Delete any old A records first, then add:

### A Records (apex domain)
| Type | Host | Value           |
|------|------|-----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

### CNAME Record (www subdomain)
| Type  | Host | Value                   |
|-------|------|-------------------------|
| CNAME | www  | YOUR-USERNAME.github.io |

DNS changes take **15 minutes to a few hours** to propagate.

---

## Making updates later

1. Edit `index.html` (all text and styling lives there)
2. Commit and push — or edit the file directly on github.com with the ✏️ pencil
3. The site updates within ~60 seconds
