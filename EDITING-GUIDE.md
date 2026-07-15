# Editing Your Site's Content on GitHub

You don't need any software installed — GitHub lets you edit files right
in your browser, and the live site updates within about a minute of saving.

## The loop

1. Open your repository on github.com.
2. Click the file you want to change (e.g. `events.html`).
3. Click the **pencil icon** in the top-right of the file view.
4. Edit the text, the same as editing a Word document.
5. Scroll down, add a short commit message, click **Commit changes**.
6. Wait about a minute, refresh your live site.

## Where to make specific changes

| What you want to change | Which file | What to look for |
|---|---|---|
| A person in the family tree (Des Raj onward) | `family-tree.html` | The `desRajNode` object |
| A name in the ancestral line (Mahiyal to Karamchand) | `family-tree.html` | The `ancestralNames` list |
| A birthday | `events.html` | The `occasions` list |
| Someone in "In Loving Memory" | `events.html` | The `inMemory` list |
| A story | `stories.html` | The `<article class="story">` blocks |
| A photo caption or album | `gallery.html` | The `albums` list |
| Text on the homepage | `index.html` | Anywhere in the visible text |

## Adding a new person to the family tree

Open `family-tree.html`, find `const desRajNode = {`. Every person looks like:

```
{ name: "Kabir Kundu", years: "b. 2005", role: "Grandson", children: [] }
```

- Give someone children by adding more of these objects inside their
  `children: [ ]` list.
- Add a sibling by copying an existing person's entire `{ ... }` block,
  including the commas around it, and editing the details.
- Every `{` needs a matching `}`, and every list item needs a comma after
  it except the last one. If the page stops working after an edit, check
  brackets and commas first — this is the most common cause.

To extend the ancestral line further back (earlier than Mahiyal), just add
more names to the start of the `ancestralNames` list — no need to touch
anything else.

## Adding a new photo

1. Create (or open) the `images` folder in your repository.
2. Use **Add file → Upload files** to add your photo there.
3. In `gallery.html`, find the relevant album and change a line like
   `file: null` to `file: "images/your-photo-name.jpg"`, matching the exact
   filename you uploaded.

## If something breaks

GitHub keeps every past version of every file. Open the file, click
**History**, and view or restore any earlier version — it's safe to
experiment.
