# Kundu Family Website — Setup Guide

This is a plain HTML/CSS/JS website — no build tools, no backend, no monthly
hosting cost. Everything below is free.

## What's in this folder

```
index.html         Home page
family-tree.html    Family tree (edit the `familyData` array to update people)
gallery.html         Photo gallery (edit the `albums` array; add real photos)
stories.html          Family stories and history
events.html            Birthdays, anniversaries, past gatherings
styles.css              Shared design system — colors, fonts, layout
```

All the content — names, dates, captions, stories — lives directly inside
the HTML files as plain text or small JavaScript lists near the bottom of
each file. You don't need to know how to code to edit it: open a file in
any text editor, find the words you want to change, and save.

---

## Step 1 — Preview it locally (optional)

Open `index.html` by double-clicking it. It works straight from your
computer, no server needed. Click through the nav to check every page.

## Step 2 — Put your real content in

- **Family tree**: open `family-tree.html`, find `const familyData = [`
  near the bottom, and edit names/years/roles. The structure is
  generation → family group → children — just follow the existing pattern.
- **Gallery**: create a folder named `images` next to the HTML files, add
  your photos there, then in `gallery.html` find `const albums = [` and
  change `file: null` to `file: "images/your-photo.jpg"` for each photo.
- **Stories**: open `stories.html` and replace the placeholder paragraphs
  inside each `<article class="story">` block.
- **Events**: open `events.html` and edit the `const occasions = [` list
  with real birthdays and anniversaries (month/day is enough).

## Step 3 — Host it for free with GitHub Pages

1. Create a free account at [github.com](https://github.com) if you don't
   have one.
2. Create a new **public** repository — name it anything, e.g. `kundu-family-site`.
3. Upload all the files in this folder to that repository (drag-and-drop
   works on GitHub's web interface — use "Add file → Upload files").
4. In the repository, go to **Settings → Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch",
   choose the `main` branch and `/ (root)` folder, then **Save**.
6. GitHub gives you a live URL like `https://yourusername.github.io/kundu-family-site`
   within a minute or two. That confirms the site works before you touch
   your domain.

*(Netlify is an equally good free alternative — drag-and-drop the folder at
[app.netlify.com/drop](https://app.netlify.com/drop) and it deploys instantly,
no GitHub account required. Either works fine with the domain steps below.)*

## Step 4 — Point kundufamily.in at it (still free)

Custom domains are free on both GitHub Pages and Netlify — you only pay
your domain registrar's yearly renewal, which you're already paying.

**On GitHub Pages:**
1. In your repository, add a file named `CNAME` (no extension) containing
   just: `kundufamily.in`
2. Still in **Settings → Pages**, enter `kundufamily.in` in the "Custom domain" field and save.
3. Go to your domain registrar (wherever you bought kundufamily.in — GoDaddy,
   Namecheap, etc.) and open its DNS settings.
4. Add these DNS records:
   - Four **A** records for `@` pointing to GitHub's IP addresses:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME** record for `www` pointing to `yourusername.github.io`
5. DNS changes take anywhere from a few minutes to 24 hours to fully
   propagate. Once it does, tick "Enforce HTTPS" back in Settings → Pages
   for a free SSL certificate.

**On Netlify** instead, the process is similar: Site settings → Domain
management → Add custom domain, and Netlify shows you the exact DNS records
to add at your registrar.

## Step 5 — Move away from Google Sites

Once `kundufamily.in` is loading your new site correctly (check from a
phone on mobile data to confirm DNS has propagated), you can safely stop
paying attention to the Google Sites version — it isn't linked to your
domain's DNS once you've repointed it, so there's nothing further to
"cancel" beyond just not updating it anymore.

---

## Updating the site later

Whenever you want to change something: edit the file, then re-upload it
to GitHub (or drag the updated folder onto Netlify again). The live site
updates within a minute — no rebuild step, no hosting fees, ever.
