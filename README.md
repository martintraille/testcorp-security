# TestCorp Security Website

Professional security testing and red team services website for TestCorp Ltd.

## 🌐 Live Website

- **Domain:** testcorpltd.com
- **Hosting:** Netlify (auto-deploys from GitHub)
- **Repository:** git@github.com:martintraille/testcorp-security.git
- **Branch:** master

## 🚀 Deployment

The website is configured for **automatic deployment** via Netlify:

1. Push changes to the `master` branch on GitHub
2. Netlify automatically detects the push and deploys
3. Changes are live within 1-2 minutes

**Note:** Currently on Netlify trial - be mindful of deployment limits.

### Manual Deployment

If needed, you can trigger a manual deploy from the Netlify dashboard:
- Login to Netlify
- Go to the TestCorp site
- Click "Trigger deploy" → "Deploy site"

## 📁 Project Structure

```
testcorp-security/
├── index.html              # Homepage with hero, services, about, contact
├── blog.html               # Blog listing page
├── careers.html            # Careers page with open positions
├── styles.css              # Main stylesheet (mobile-first design)
├── animations.css          # Animation styles
├── script.js               # JavaScript for interactions and mobile menu
├── BLOG-INSTRUCTIONS.md    # Instructions for adding blog posts
├── blog/                   # Individual blog post pages
│   ├── essential-web-app-security.html
│   ├── red-team-vs-pentest.html
│   └── security-testing-checklist.html
└── services/               # Individual service pages
    ├── penetration-testing.html
    ├── red-team-operations.html
    ├── security-consulting.html
    ├── code-review.html
    ├── cloud-security.html
    └── compliance-testing.html
```

## 🎨 Design System

### Color Palette
- **Primary:** `#0a192f` (Dark navy blue)
- **Secondary:** `#64ffda` (Bright cyan/green)
- **Accent:** `#f06449` (Coral red)
- **Text:** `#e6f1ff` (Light blue-white)
- **Muted Text:** `#8892b0` (Blue-gray)
- **Background:** `#020c1b` (Very dark blue)
- **Card Background:** `#112240` (Dark blue)

### Layout
- **Max Width:** 1200px (consistent across all pages)
- **Mobile Breakpoint:** 1024px (hamburger menu appears)
- **Small Mobile:** 480px (additional text size adjustments)

## 🔧 Local Development

### Quick Start

1. Clone the repository:
```bash
git clone git@github.com:martintraille/testcorp-security.git
cd testcorp-security
```

2. Start a local web server:
```bash
python3 -m http.server 8000
```

3. Open in browser:
```
http://localhost:8000
```

### Testing on Mobile Devices

To test on your iPhone/iPad on the same WiFi network:

1. Start the local server (see above)

2. Get your Mac's local IP address:
```bash
ipconfig getifaddr en0
```

3. On your mobile device, open Safari and go to:
```
http://[YOUR-IP-ADDRESS]:8000
```

Example: `http://192.168.68.77:8000`

## 📱 Mobile Menu

The mobile hamburger menu appears at screen widths **≤1024px**.

**How it works:**
- JavaScript toggles the `.active` class on both the menu and toggle button
- CSS handles the show/hide with `display: none/flex`
- Menu drops down from header with absolute positioning
- Smooth animations for opening/closing

**Recent Fix:** Fixed duplicate JavaScript variable declarations that were preventing the menu from working (see commit history).

## 📝 Content Management

### Adding Blog Posts

See [BLOG-INSTRUCTIONS.md](BLOG-INSTRUCTIONS.md) for detailed instructions on adding new blog posts.

Quick steps:
1. Create new HTML file in `blog/` directory
2. Add blog card to `blog.html` with link, title, excerpt, date, and category
3. Blog posts use SVG icons matching the services page style

### Forms

Forms are connected to **Formspree** for handling submissions:
- Contact form (index.html)
- Careers application form (careers.html)

Forms submit directly to Formspree endpoints - no backend code needed.

## 🛠️ Technical Details

### Icons
- Logo: Shield emoji (🛡️)
- Service/blog icons: Custom SVG icons (stroke-based, 64x64px)
- All icons use `var(--secondary-color)` for consistent theming

### Typography
- Font: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
- Headings: Bold, colored with secondary color
- Body: Light text on dark background for cybersecurity aesthetic

### JavaScript Features
- Mobile menu toggle
- Smooth scrolling for anchor links
- Scroll-based animations (fade-in, counter animations)
- Parallax effects on hero section
- Form submission handling (via Formspree)
- Ripple effects on buttons

## 🐛 Troubleshooting

### Mobile Menu Not Working
- Clear browser cache (hard refresh)
- Check for JavaScript errors in console
- Verify no duplicate `const` declarations in script.js
- Test on localhost first before deploying

### Netlify Deployment Issues
- Check Netlify dashboard for build errors
- Verify GitHub repository is connected
- Check branch name is correct (master)
- Review deployment logs in Netlify

### Forms Not Submitting
- Verify Formspree endpoints are active
- Check Formspree dashboard for submission logs
- Ensure form action URLs are correct

## 📄 Pages

### Main Pages
- **Homepage** (index.html) - Hero, services overview, about, stats, contact
- **Blog** (blog.html) - Blog post listing with 3 sample posts
- **Careers** (careers.html) - Open positions, benefits, company values

### Service Pages (in services/)
- Penetration Testing
- Red Team Operations
- Security Consulting
- Code Review
- Cloud Security Assessment
- Compliance Testing

### Legal Pages
- Privacy Policy
- Terms of Service
- Responsible Disclosure

## 🔐 Security

This is a security company website, so security best practices are followed:
- No sensitive data stored in repository
- Forms handled via secure third-party (Formspree)
- HTTPS enforced via Netlify
- No client-side storage of user data

## 📋 Git Workflow

### Committing Changes

```bash
# Check status
git status

# Add changes
git add .

# Commit with descriptive message
git commit -m "Your descriptive message"

# Push to GitHub (triggers Netlify deploy)
git push origin master
```

### Recent Updates
- Fixed mobile hamburger menu (removed duplicate JS declarations)
- Replaced emoji icons with SVG icons across blog and careers pages
- Added Blog link to navigation across all pages
- Fixed careers page width consistency (1200px)
- Aligned careers page icons to left (matching services)

## 📞 Contact

For website updates or questions, contact Martin Traille.

---

**Last Updated:** October 2025
