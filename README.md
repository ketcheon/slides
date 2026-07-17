# Deck Builder for GitHub Pages

This mini app lets non-technical users create Reveal.js decks from simple text, then either:

- preview instantly in browser
- copy a share URL
- download a standalone HTML slideshow file

## Two ways friends can use it

1. Use your hosted repo directly
2. Host their own copy

### 1) Use your hosted repo directly

- You host this app once on your GitHub Pages.
- Friends open your hosted index.html.
- For cleaner separation, each friend/project uses a project URL like:
	- index.html?project=alice-youth
	- index.html?project=bob-weekly
- They create/edit deck text and run preview.
- They can export standalone deck HTML for TV playback.

How URL and naming works in this mode:

- They do get a different URL per project, using only query parameter.
- Base hosting URL stays the same; only ?project=... changes.
- They can switch project from the in-app project switcher (no manual URL editing needed).
- Data is stored per project key in browser local storage.
- Downloaded files are prefixed as project--deck-title.html.

### 2) Host their own copy

- Friends copy index.html and slideshow.html into their own GitHub repo.
- They enable GitHub Pages in that repo.
- They run everything from their own URL and account.
- Their deck data stays in their own browser storage.

## Files

- index.html -> admin/editor interface
- slideshow.html -> presentation player for encoded deck links

## Quick start

1. Open index.html in your browser.
2. Create or edit a deck.
3. Click Save.
4. Click Preview to test.
5. Click Download Standalone HTML to get a single file you can publish.

Optional: add ?project=my-team in URL before editing to isolate project decks.

In-app switcher:

- Use the dropdown to select existing project keys.
- Or type a new key (example: youth-aug) and click Open Project.
- The app automatically opens the correct URL with ?project=your-key.

## Publish to GitHub Pages

Option A: share dynamic deck links from this app

1. Put both index.html and slideshow.html in a GitHub repo.
2. Enable GitHub Pages for that repo.
3. Open the hosted index.html, click Copy Share Link, and send the URL.

Option B: publish a standalone deck file

1. In the builder, click Download Standalone HTML.
2. Put the downloaded file into any GitHub Pages repo.
3. Open that file URL directly on TV browser.

## Friend-friendly workflow

Each friend can fork or copy these two files into their own repo and use their own GitHub account:

1. Create a new public repo (for example: my-slides).
2. Upload index.html and slideshow.html.
3. Enable Pages from branch main, root.
4. Open the hosted index.html and start building decks.

No local install or backend is required.
