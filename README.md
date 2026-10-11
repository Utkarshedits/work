# Utkarsh Khobragade — Portfolio

A single-page video-editor portfolio. It's plain HTML, CSS and JavaScript with no build step, so it can be hosted on GitHub Pages as-is.

```
index.html   ← the whole site (styles + script inline)
assets/      ← thumbnails and client logos (.webp)
.nojekyll    ← tells GitHub Pages to serve files as-is
```

## Host it on GitHub Pages

1. On GitHub, open the repo and go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Pick the branch that holds `index.html` (for example `main`) and the folder **`/ (root)`**, then click **Save**.
4. Wait a minute or two. The site will be live at `https://<github-username>.github.io/<repo-name>/`.

## Make it your own (for a new owner)

### 1. Get your own copy

Pick one:

- **Fork (easiest):** while signed in to your own GitHub account, open this repo and click **Fork**.
- **Fresh copy (no link to this repo):**
  1. Create a new empty repo on your account, e.g. `my-portfolio`.
  2. Run:
     ```bash
     git clone https://github.com/oshal7/Utkarsh-Port.git my-portfolio
     cd my-portfolio
     git remote set-url origin https://github.com/<your-username>/my-portfolio.git
     git push -u origin --all
     ```

> Tip: if you name the repo exactly `<your-username>.github.io`, the site is served at `https://<your-username>.github.io/` with no extra path.

### 2. Edit the content

Everything to change is in `index.html`:

| What | Where |
| --- | --- |
| Browser tab title | `<title>` at the top of the file |
| Email, WhatsApp, LinkedIn, Instagram | `const CONTACT = {...}` (search for `Edit contact details here`) |
| Clients (name, description, logo, channel link) | `const CLIENTS = {...}` |
| Showcase videos (YouTube ID, title, category, client) | `const VIDEOS = [...]` |
| Name, bio, and other text | Search the HTML for the text you want to change |

Thumbnails live in `assets/`. A video entry with `img:"abc123"` loads `assets/abc123.webp`, so add your image with a matching name.

### 3. Preview locally (optional)

Open `index.html` in a browser, or run a small server from the repo folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

### 4. Publish

```bash
git add .
git commit -m "Update portfolio content"
git push
```

Then turn on GitHub Pages in **your** repo using the steps in [Host it on GitHub Pages](#host-it-on-github-pages). Every later push updates the live site within a minute or two.
