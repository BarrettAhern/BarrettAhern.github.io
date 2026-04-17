# barrettahern.com

Personal website for Barrett Ahern — built with plain HTML & CSS, hosted on GitHub Pages.

---

## File structure

```
barrettahern.com/
├── index.html        ← Homepage
├── about.html        ← About Me page
├── work.html         ← Case Studies / Work page
├── css/
│   └── style.css     ← All styles (one file, well-commented)
├── images/           ← Put your own images here
└── README.md         ← This file
```

---

## How to set up GitHub Pages (one-time)

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository** (the + icon, top right)
3. Name it exactly: `barrettahern.com` (or any name you like)
4. Set it to **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2 — Upload the files

Option A — drag and drop (easiest to start):
1. Open your new repo on GitHub
2. Click **Add file → Upload files**
3. Drag all the files and folders in, keeping the folder structure intact
4. Click **Commit changes**

Option B — use Git from the terminal (better long-term):
```bash
# Navigate to this folder in your terminal
cd path/to/barrettahern.com

# Initialise a git repo
git init

# Link it to GitHub (replace YOUR_USERNAME with yours)
git remote add origin https://github.com/YOUR_USERNAME/barrettahern.com.git

# Stage all files
git add .

# Make your first commit
git commit -m "Initial site build"

# Push to GitHub
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. In your repo, go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**
5. After a minute, GitHub will show you a URL like `https://yourusername.github.io/barrettahern.com`

### Step 4 — Connect your custom domain

1. In **Settings → Pages → Custom domain**, enter: `barrettahern.com`
2. Click **Save** — this creates a `CNAME` file in your repo automatically
3. Log in to wherever your domain is registered (e.g. GoDaddy, Namecheap)
4. Update DNS records to point to GitHub:
   - Add 4 A records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Add a CNAME record: `www` → `yourusername.github.io`
5. DNS changes can take up to 24 hours to propagate
6. Back in GitHub Pages settings, tick **Enforce HTTPS** once it appears

---

## How to make edits (the workflow)

Every change follows this pattern:

```
Edit file → Save → Commit → Push → Site updates automatically
```

### Using Claude (Cowork)

Just ask Claude to make the change. For example:
- "Update the bio on about.html to say..."
- "Add a new case study card to work.html for [client]"
- "Change the footer email address"

Claude will edit the file directly in this folder. Then you commit and push to GitHub.

### Using Git to save and publish changes

```bash
# See what changed
git status

# Stage the changed file(s)
git add about.html

# Or stage everything
git add .

# Write a short message describing what you changed
git commit -m "Update bio text"

# Publish to GitHub (site updates within ~1 minute)
git push
```

### Key Git commands to know

| Command | What it does |
|---|---|
| `git status` | Shows which files have changed |
| `git diff` | Shows exactly what changed, line by line |
| `git add filename` | Stages a file to be committed |
| `git add .` | Stages all changed files |
| `git commit -m "message"` | Saves a snapshot with a description |
| `git push` | Sends your commits to GitHub |
| `git log --oneline` | Shows recent commit history |
| `git pull` | Gets the latest changes from GitHub |

---

## Common edits

### Change text on the homepage
Open `index.html`. The content is in clearly labelled sections with HTML comments like `<!-- HERO -->`, `<!-- SERVICES -->`, etc. Find the text you want to change and edit it.

### Add a new case study card
Open `work.html`. Copy an existing `<a class="card">` block and update the `href`, `src` (image), label, and title.

### Change a colour or font size
Open `css/style.css`. All the core values are defined at the top in `:root { }` as CSS variables — no need to hunt through the file.

### Add your own photo
1. Save your image as `images/barrett_ahern.jpg`
2. In `index.html`, find the `<img>` in the hero section
3. Change `src="https://barrettahern.com/..."` to `src="images/barrett_ahern.jpg"`

---

## Images note

Currently, the logo and case study images are loaded directly from the WordPress site URLs. This works fine for now, but once you cancel WordPress hosting you'll want to:

1. Download each image from the WordPress URLs
2. Save them into the `images/` folder
3. Update the `src` attributes in the HTML to use `images/filename.ext`

---

## Questions / things to try next

- Add a `favicon.ico` (the little icon in the browser tab)
- Add Google Analytics for traffic tracking
- Add Open Graph meta tags so links look good when shared on social
- Improve accessibility with better colour contrast
- Add smooth hover transitions to more elements
