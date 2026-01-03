# Deployment Guide

## Option 1: Deploy to Vercel (Recommended - Easiest)

Vercel is made by the creators of Next.js and offers the simplest deployment experience.

### Steps:

1. **Push your code to GitHub** (if not already done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin YOUR_GITHUB_REPO_URL
   git push -u origin main
   ```

2. **Deploy to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Sign up/login (can use GitHub account)
   - Click "Add New Project"
   - Import your GitHub repository
   - Vercel will auto-detect Next.js settings
   - Click "Deploy"
   - Your app will be live in ~2 minutes!

3. **That's it!** Vercel will give you a URL like: `your-app-name.vercel.app`

### Using Vercel CLI (Alternative):

```bash
npm i -g vercel
vercel
```

Follow the prompts and your app will be deployed.

---

## Option 2: Deploy to Netlify

1. **Push code to GitHub** (same as above)

2. **Deploy to Netlify**:
   - Go to [netlify.com](https://netlify.com)
   - Sign up/login
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Build settings:
     - Build command: `npm run build`
     - Publish directory: `.next`
   - Click "Deploy site"

---

## Option 3: Deploy to Other Platforms

### Railway:
- Go to [railway.app](https://railway.app)
- Connect GitHub repo
- Auto-detects Next.js

### Render:
- Go to [render.com](https://render.com)
- Connect GitHub repo
- Build command: `npm install && npm run build`
- Start command: `npm start`

### Self-hosted (VPS):
- Build: `npm run build`
- Start: `npm start`
- Requires Node.js 18+ on server

---

## Pre-deployment Checklist

✅ Code builds successfully (`npm run build`)
✅ No linting errors (`npm run lint`)
✅ Test locally (`npm run dev`)
✅ All dependencies in `package.json`
✅ `.gitignore` excludes `node_modules` and `.next`

---

## Notes

- Vercel is recommended for Next.js apps (zero configuration)
- Free tier available on all platforms
- Automatic HTTPS included
- Custom domains supported
- Automatic deployments on git push (if connected to GitHub)
