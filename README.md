# React Artifact Template

Quick template for publishing React artifacts from Claude to GitHub Pages.

## Quick Start

1. **Clone this template**
```bash
   cp -r react-template my-new-project
   cd my-new-project
```

2. **Update project name**
   - In `package.json`: Change `"name"` to your project name
   - In `vite.config.js`: Update `base: '/your-repo-name/'`

3. **Replace the app**
   - Paste your Claude artifact code into `src/App.jsx`

4. **Install dependencies**
```bash
   npm install
```

5. **Test locally**
```bash
   npm run dev
```

6. **Create GitHub repo and deploy**
```bash
   git remote set-url origin https://github.com/YOUR-USERNAME/your-repo-name.git
   git add .
   git commit -m "Initial commit"
   git push -u origin main
   npm run deploy
```

7. **Enable GitHub Pages**
   - Go to repo Settings → Pages
   - Select `gh-pages` branch
   - Save

## Files Included

- Vite + React setup
- Tailwind CSS configured
- GitHub Pages deployment script
- All dependencies pre-configured for Node 17+

## Update Deployments
```bash
git add .
git commit -m "Update"
git push
npm run deploy
```