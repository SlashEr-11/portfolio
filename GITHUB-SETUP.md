# 🚀 Quick Setup Guide: Connect Your Portfolio to GitHub

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named: `portfolio` (or any name you prefer)
3. **DO NOT** initialize with README, .gitignore, or license (we already have them)
4. Click "Create repository"

## Step 2: Connect Your Local Project to GitHub

Copy and paste these commands in your terminal:

```bash
cd "c:\Users\hp -pc\Desktop\Projects Stuffs\portfolio"

# Add your GitHub repository (REPLACE with your actual repo URL)
git remote add origin https://github.com/SlashEr-11/portfolio.git

# Push your code to GitHub
git push -u origin main
```

**Important:** Replace `SlashEr-11` with your actual GitHub username if different, and replace `portfolio` with your repository name.

## Step 3: Enable GitHub Pages (Optional - for free hosting)

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select: **main** branch
4. Select folder: **/ (root)**
5. Click **Save**
6. Your portfolio will be live at: `https://your-username.github.io/portfolio/modern.html`

## 🔄 Auto-Sync Workflow (Future Updates)

Whenever you make changes, just run these 3 commands:

```bash
git add .
git commit -m "Update TryHackMe stats"
git push origin main
```

Your changes will automatically appear on GitHub and your live website!

## 📝 Common Update Commands

### Update TryHackMe stats:
```bash
# Edit tryhackme-data.json with your latest stats
git add tryhackme-data.json
git commit -m "Update TryHackMe stats - $(date +%Y-%m-%d)"
git push origin main
```

### Update portfolio content:
```bash
git add modern.html
git commit -m "Update portfolio content"
git push origin main
```

### Update everything:
```bash
git add .
git commit -m "Update portfolio - $(date +%Y-%m-%d)"
git push origin main
```

## 🆘 Troubleshooting

### If you get authentication errors:
1. Use **Personal Access Token** instead of password
2. Generate token: GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
3. Select scopes: `repo`, `workflow`
4. Use token as password when prompted

### If repository already exists:
```bash
git remote remove origin
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

---

## ✅ Current Status:

- ✅ Git initialized
- ✅ Initial commit created (7 files)
- ✅ README.md created
- ✅ .gitignore configured
- ⏳ **Next:** Connect to GitHub remote
- ⏳ **Then:** Push to GitHub

---

**Your Local Repository Info:**
- Branch: `main`
- Latest commit: "Initial commit: Portfolio with TryHackMe integration"
- Files tracked: 7 files, 1204 lines

**Ready to connect to GitHub!** 🚀
