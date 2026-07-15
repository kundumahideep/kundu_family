# Kundu Parivar Website — Setup Guide

Plain HTML/CSS/JS — no build tools, no backend, no monthly hosting cost.

## What's in this folder

```
index.html         Home page
family-tree.html    Family tree — twenty-six generations, edit desRajNode / ancestralNames to update people
gallery.html         Photo gallery — edit the `albums` array; add real photos
stories.html          Family stories and history
events.html            Birthdays, past gatherings, and an in-memory section
styles.css              Shared design system — colors, fonts, layout
```

## Uploading this update to GitHub (replacing the old version)

Since every file here keeps its original name, you don't need to delete
anything first:

1. Go to your repository on github.com.
2. Click **Add file → Upload files**.
3. Drag in every file from this folder (including `styles.css`).
4. Scroll down and click **Commit changes**.

GitHub will ask to confirm you're replacing existing files with the same
names — confirm, and your site updates within about a minute.

## What changed in this version

- **New design direction**: an elegant, formal "family register" look —
  deep green and oxblood with brass gold accents, formal serif type,
  instead of the earlier warm/rustic style.
- **Family tree**: now includes the full twenty-two-generation ancestral
  line (Mahiyal through Karamchand) leading to Ch. Des Raj Kundu and his
  four generations of descendants — branching properly on desktop, and
  collapsible generation-by-generation on mobile.
- **Events page**: real birthdays for every family member with a known
  date, plus a respectful "In Loving Memory" section for those who have
  passed, separate from the birthday list.
- **Search**: you can now search any name on the Family Tree page and it
  will highlight the match and auto-expand its way there.

## Still coming

The "+ Add / Edit" buttons on each family tree card are placeholders for
now — the plan is for these to open a small form that emails you for
approval before anything changes on the live site, so edits never require
opening GitHub. That feature is being designed next and will replace these
buttons once ready.

## Editing content later

See `EDITING-GUIDE.md` for the walkthrough on editing any page directly
from GitHub's website, with no software to install.
