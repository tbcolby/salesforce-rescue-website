# Salesforce Rescue Website - Deployment Guide

## Option 1: Netlify Drop (Fastest - 30 seconds)

1. Go to https://app.netlify.com/drop
2. Drag the entire `/Website` folder onto the drop zone
3. Your site is live immediately with a random URL
4. Optional: Change the site name in Netlify settings
5. Optional: Add a custom domain

**Pros:** Instant, zero config, free HTTPS
**Cons:** Random URL initially

---

## Option 2: Netlify CLI (Recommended - 2 minutes)

```bash
# Install Netlify CLI (if needed)
npm install -g netlify-cli

# Navigate to the website directory
cd "/Users/tyler/Salesforce Rescue/Website"

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod
```

When prompted:
- Create new site: Yes
- Path to deploy: `.` (current directory)

**Pros:** CLI control, easy updates, custom domain setup
**Cons:** Requires npm and Netlify account

---

## Option 3: GitHub Pages (5 minutes)

```bash
# Create a new GitHub repo
cd "/Users/tyler/Salesforce Rescue/Website"
git init
git add .
git commit -m "Initial Salesforce Rescue website

Co-Authored-By: Warp <agent@warp.dev>"
gh repo create salesforce-rescue-website --public --source=. --push

# Enable GitHub Pages
gh api repos/tyler/salesforce-rescue-website/pages -X POST -f source[branch]=main -f source[path]=/
```

Site will be live at: `https://tyler.github.io/salesforce-rescue-website`

**Pros:** Free, version controlled, GitHub integration
**Cons:** Slightly slower, requires GitHub CLI

---

## Option 4: Vercel (2 minutes)

```bash
# Install Vercel CLI (if needed)
npm install -g vercel

# Navigate and deploy
cd "/Users/tyler/Salesforce Rescue/Website"
vercel --prod
```

**Pros:** Fast CDN, great performance, free SSL
**Cons:** Requires Vercel account

---

## Next Steps After Deployment

1. **Update Calendly Link**: Replace `https://calendly.com/your-calendly-link` in `index.html` line 272 with your actual Calendly URL

2. **Add Custom Domain** (optional):
   - Purchase domain (e.g., salesforcerescue.com)
   - Add DNS records in your hosting platform
   - Enable SSL (automatic on Netlify/Vercel)

3. **Set Up Analytics** (optional):
   - Google Analytics
   - Plausible Analytics
   - Simple Analytics

4. **Test on Mobile**: Open the live URL on your phone to verify responsive design

---

## Recommended: Start with Netlify Drop

For getting live TODAY, I recommend:
1. Use Netlify Drop first (instant)
2. Update Calendly link
3. Share with first potential clients
4. Iterate based on feedback
5. Add custom domain when ready

The site is already mobile-responsive, SEO-optimized, and production-ready.
