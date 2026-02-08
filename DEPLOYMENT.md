# Deployment Guide for Clean My Prompt

## 🚀 Quick Deploy to Cloudflare

### Prerequisites
```bash
npm install -g wrangler
wrangler login
```

### Deploy Command
```bash
npx wrangler deploy
```

That's it! Your site will be live at `https://cleanmyprompt.<your-subdomain>.workers.dev`

---

## 📝 What Gets Deployed

All files in the root directory:
- ✅ index.html (main app)
- ✅ about.html, how-it-works.html, cookie-policy.html, privacy-policy.html, terms-of-service.html
- ✅ Clean My Prompt.svg, favicon.svg, favicon.ico
- ✅ sitemap.xml, robots.txt
- ✅ README.md, LICENSE

---

## 🌐 Alternative Deployment Options

### Option 1: GitHub Pages (Free)
1. Go to repository Settings → Pages
2. Source: Deploy from branch `main`
3. Directory: `/` (root)
4. Save

**Live URL:** `https://eulex0x.github.io/cleanmyprompt/`

### Option 2: Netlify (Free)
1. Import Git repository
2. Build command: (leave empty)
3. Publish directory: `/`
4. Deploy

**Features:** Instant deploy on git push, custom domain, free SSL

### Option 3: Vercel (Free)
1. Import GitHub repository
2. Framework Preset: Other
3. Build Command: (leave empty)
4. Output Directory: `./`
5. Deploy

**Features:** Edge network, automatic HTTPS, preview deployments

### Option 4: Cloudflare Pages (Alternative to Workers)
1. Dashboard → Pages → Create a project
2. Connect GitHub repository
3. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: `/`
4. Deploy

**Difference from Workers:** Pages is optimized for static sites, Workers is more flexible

---

## 🔧 Custom Domain Setup

### Cloudflare
1. Add domain in dashboard
2. Update DNS records automatically
3. SSL certificate auto-issued

### GitHub Pages
1. Settings → Pages → Custom domain
2. Add CNAME record: `<your-domain>` → `eulex0x.github.io`
3. Enable HTTPS

### Netlify/Vercel
1. Add custom domain in dashboard
2. Follow DNS configuration instructions
3. SSL automatic

---

## ✅ Post-Deployment Checklist

- [ ] Test main app: `https://your-domain/`
- [ ] Test all pages load correctly
- [ ] Verify favicon displays
- [ ] Check sitemap.xml accessibility
- [ ] Test offline mode (disconnect internet, reload page)
- [ ] Submit sitemap to Google Search Console
- [ ] Test "Try Demo" button functionality
- [ ] Verify all GitHub links point to `Eulex0x/cleanmyprompt`
- [ ] Check mobile responsiveness
- [ ] Test theme toggle (dark/warm)

---

## 📊 Expected Performance

**Cloudflare Workers/Pages:**
- Global CDN: <50ms response time worldwide
- 100% uptime SLA
- Unlimited bandwidth (free tier)
- DDoS protection included

**GitHub Pages:**
- GitHub's CDN
- 100GB bandwidth/month (soft limit)
- Free SSL
- 10 builds/hour limit

**Netlify/Vercel:**
- Edge network (100+ locations)
- 100GB bandwidth/month (free tier)
- Automatic deployments on git push
- Preview URLs for PRs

---

## 🐛 Troubleshooting

**Issue:** Pages not loading
- Check build output directory is set to `/` or `./`
- Verify all files are committed to Git

**Issue:** Styling not working
- Check if CSS CDNs are accessible (Tailwind, Google Fonts)
- Verify no Content Security Policy blocking external resources

**Issue:** Logo not displaying
- Ensure `Clean My Prompt.svg` is in root directory
- Check file permissions (should be readable)

**Issue:** Offline popup not showing
- This is expected - offline detection only works after initial page load
- Disconnect internet, then reload page

---

## 💰 Cost Comparison

| Platform | Free Tier | Bandwidth | Builds | Custom Domain |
|----------|-----------|-----------|--------|---------------|
| **Cloudflare Workers** | 100k req/day | Unlimited | Unlimited | Yes (free) |
| **Cloudflare Pages** | Unlimited | Unlimited | 500/month | Yes (free) |
| **GitHub Pages** | Unlimited | 100GB/month | Unlimited | Yes (free) |
| **Netlify** | Unlimited | 100GB/month | 300 min/month | Yes (free) |
| **Vercel** | Unlimited | 100GB/month | Unlimited | Yes (free) |

**Recommendation:** Cloudflare Pages or Workers (best performance + no limits)

---

## 🎉 Your Site is Live!

Once deployed, share your link:
- Twitter/X: "Check out Clean My Prompt - privacy-first AI prompt sanitizer!"
- Reddit: r/privacy, r/webdev, r/opensource
- Hacker News: Share in Show HN
- Product Hunt: Launch your product

Don't forget to update the canonical URLs in meta tags if using a custom domain!
