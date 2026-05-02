# Vercel Deployment Guide

## Project Structure

Your project is now optimized for Vercel deployment with the following structure:

```
Marketing plan/
├── index.html                 # Main HTML file
├── vercel.json               # Vercel configuration
├── public/
│   └── assets/
│       ├── images/
│       │   └── hamper.jpg    # Add your hamper product image here
│       └── logos/
│           ├── logo-01.jpg
│           ├── logo-02.jpg
│           ├── logo-03.jpg
│           ├── logo-04.jpg
│           ├── logo-05.jpg
│           ├── logo-06.jpg
│           ├── logo-07.jpg
│           ├── logo-08.jpg
│           ├── logo-09.jpg
│           ├── logo-10.jpg
│           └── logo-11.jpg
└── DEPLOYMENT_GUIDE.md       # This file
```

## What's Been Updated

### 1. **Image Paths**
   - Changed from: `merch/hamper.jpg` → `src="/assets/images/hamper.jpg"`
   - All image paths now use absolute `/assets/` paths, which work perfectly with Vercel's static hosting
   - Logo files are organized in `public/assets/logos/`

### 2. **Budget Section**
   - ✅ Added new **Starter Package (₹5,000/month)** with:
     - **Post Boosting**: ₹3,000 (60%)
     - **Content Creation**: ₹2,000 (40%)
   - Existing ₹35,000 budget remains intact
   - Both budgets display with proper visual hierarchy

### 3. **Vercel Configuration** (`vercel.json`)
   - Static site optimization
   - Image caching headers (1 year for assets)
   - HTML page caching (1 hour for updates)
   - Ready for production deployment

## How to Deploy to Vercel

### Step 1: Prepare Your Files
1. **Add your hamper image**:
   - Save your hamper product photo as: `public/assets/images/hamper.jpg`
   - Recommended: JPEG format, optimized for web (max 500KB)

2. **Logo images** are already in place:
   - Located in: `public/assets/logos/`
   - 11 logo options ready to use

### Step 2: Deploy to Vercel

#### Option A: Using Vercel CLI (Recommended)
```bash
# Install Vercel CLI (if not already installed)
npm install -g vercel

# In your project directory
vercel
```
Follow the prompts to:
- Login/create Vercel account
- Import your project
- Deploy

#### Option B: Using Git
1. Push your project to GitHub (or GitLab/Bitbucket)
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your repository
5. Vercel auto-detects the settings (thanks to `vercel.json`)
6. Click "Deploy"

#### Option C: Drag & Drop
1. Go to [vercel.com](https://vercel.com)
2. Drag and drop your entire `Marketing plan` folder
3. Done! Your site is live

### Step 3: Custom Domain (Optional)
1. In Vercel dashboard → Your project → Settings → Domains
2. Add your custom domain (e.g., `tiqinteriors.com`)
3. Follow DNS setup instructions

## File Paths for Reference

| File | Path | Purpose |
|------|------|---------|
| Main Page | `/index.html` | Your dashboard |
| Hamper Image | `/assets/images/hamper.jpg` | Product showcase |
| Logo Options | `/assets/logos/logo-01.jpg` through `logo-11.jpg` | Brand assets |
| Config | `/vercel.json` | Deployment settings |

## Image Optimization Tips

For best Vercel performance:
- Keep images under 1MB each
- Use JPEG for photos, PNG for graphics
- Consider WebP format for modern browsers
- Lazy loading is already enabled (`loading="lazy"`)

## Testing Before Deployment

Before deploying:
1. Open `index.html` in your browser
2. Verify all images load correctly
3. Check that budget section displays properly
4. Test on mobile devices
5. Verify links work correctly

## Troubleshooting

### Images not loading after deployment?
- Verify file paths use `/assets/` prefix (they do now ✅)
- Ensure hamper image is saved at `public/assets/images/hamper.jpg`
- Check file names match exactly (case-sensitive)

### Budget section looks wrong?
- Clear browser cache (Ctrl+Shift+Delete)
- Hard refresh the page (Ctrl+Shift+R)

### Need to update content?
- Edit `index.html` locally
- Git push (if using GitHub) or redeploy
- Changes live within seconds

## Support

- Vercel Docs: https://vercel.com/docs
- Static Site Hosting: https://vercel.com/docs/concepts/deployments/static-exports

---

**Your site is now Vercel-ready!** 🚀
