# Nodo App Roadmap — GitHub Setup

## Quick Start (5 minutes)

### 1. Create a GitHub repo
- Go to https://github.com/new
- Name it `nodo-roadmap` (or whatever you like)
- Set it to **Public** (required for free GitHub Pages)
- Click **Create repository**

### 2. Upload the files
Upload both files to the root of the repo:
```
nodo-roadmap/
  ├── index.html
  └── data.json
```

You can drag and drop them on the GitHub page, or use git:
```bash
git clone https://github.com/YOUR-USERNAME/nodo-roadmap.git
cd nodo-roadmap
# copy index.html and data.json here
git add .
git commit -m "Initial roadmap"
git push
```

### 3. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under "Source", select **Deploy from a branch**
- Branch: `main`, folder: `/ (root)`
- Click **Save**
- Your roadmap will be live at: `https://YOUR-USERNAME.github.io/nodo-roadmap/`

### 4. Create a GitHub Token (for admin editing)
- Go to https://github.com/settings/tokens/new
- Name: `Nodo Roadmap`
- Scope: check `repo` (full control)
- Click **Generate token**
- Copy the token — you'll need it for the admin panel

### 5. Using the Admin Panel
1. Open your roadmap URL
2. Click the **gear icon** (top right)
3. Enter your repo (e.g., `yourname/nodo-roadmap`)
4. Paste your GitHub token
5. Branch: `main` (default)
6. Click **Connect**
7. Now click any task bar to edit status, assignee, and notes
8. Changes save automatically to your repo

## Adding Team Members

Edit `data.json` and add people to the `team` array:
```json
"team": [
  { "id": "taina", "name": "Taina", "initials": "TR", "color": "#3BB1BD" },
  { "id": "carlos", "name": "Carlos", "initials": "CG", "color": "#9B6DD7" },
  { "id": "maria", "name": "María", "initials": "MR", "color": "#E8A838" }
]
```

## Task Statuses
- `pending` — Not started (gray dot)
- `in_progress` — Currently active (blue pulsing dot)
- `done` — Completed (green dot, bar fades slightly)
- `behind` — Behind schedule (red pulsing dot, red border on bar)

## Sharing with your team
Share the GitHub token with your small team, or create individual tokens for each person. Anyone with the URL can **view** the roadmap — only people with tokens can **edit** it.
