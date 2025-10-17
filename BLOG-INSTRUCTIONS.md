### How to Add New Blog Posts

This guide will help you easily add new blog articles to your TestCorp website.

## Quick Overview

1. Create a new HTML file in the `/blog` folder
2. Add the article entry to `blog.html`
3. That's it! Your new post is live.

---

## Step-by-Step Instructions

### Step 1: Create Your Blog Post HTML File

1. **Copy the sample blog post** as a template:
   - Navigate to `/blog/common-web-app-vulnerabilities-2024.html`
   - Save it with a new filename (use hyphens, lowercase)
   - Example: `blog/my-new-article-title.html`

2. **Update the following sections** in your new file:

#### A. Page Title (line 6)
```html
<title>Your Article Title - TestCorp Blog</title>
```

#### B. Post Metadata (around line 111-115)
```html
<span class="post-date">📅 16 October 2024</span>
<span class="post-category">🔒 Your Category</span>
<span class="post-author">✍️ Author Name</span>
```

#### C. Article Header (around line 117-118)
```html
<h1>Your Article Title</h1>
<p class="post-excerpt">Your article summary/excerpt goes here.</p>
```

#### D. Article Content (around line 122 onwards)
- Replace all the sample content with your article
- Keep the HTML structure (h2, h3, p, ul, ol tags)
- Use the provided styles

3. **Save the file** in the `/blog` folder

---

### Step 2: Add Your Article to the Blog Homepage

1. **Open `blog.html`** in your editor

2. **Find the section** that says `<!-- BLOG POST 1 - Sample Article -->` (around line 68)

3. **Add your new article card** at the top of the blog grid (right after the opening `<div class="blog-grid">` tag):

```html
<!-- YOUR NEW BLOG POST -->
<article class="blog-card">
    <a href="blog/your-article-filename.html" style="text-decoration: none; color: inherit; display: flex; flex-direction: column; height: 100%;">
        <div class="blog-image">🔒</div>  <!-- Change emoji to match your topic -->
        <div class="blog-content">
            <div class="blog-meta">
                <span class="blog-date">16 October 2024</span>
                <span class="blog-category">Your Category</span>
                <span class="blog-read-time">5 min read</span>
            </div>
            <h3>Your Article Title</h3>
            <p class="blog-excerpt">Your article summary goes here. Keep it to 2-3 sentences.</p>
            <span class="read-more">Read More →</span>
        </div>
    </a>
</article>
```

4. **Customize the card:**
   - Change the emoji icon (options: 🔒🎯⚡🛡️🔐💻🚀📊🌐⚔️)
   - Update the date
   - Update the category
   - Update the reading time (estimate: ~200 words per minute)
   - Update the title and link
   - Update the excerpt

5. **Save `blog.html`**

---

## Example Workflow

Let's say you want to write an article called "5 Tips for Secure Cloud Configuration"

### Step 1: Create the Article File

1. Copy `blog/common-web-app-vulnerabilities-2024.html`
2. Save as `blog/5-tips-secure-cloud-configuration.html`
3. Update:
   - Title: "5 Tips for Secure Cloud Configuration - TestCorp Blog"
   - Date: "20 October 2024"
   - Category: "Cloud Security"
   - Author: "TestCorp Security Team"
   - Heading: "5 Tips for Secure Cloud Configuration"
   - Excerpt: "Learn essential security practices for cloud infrastructure..."
   - Content: Write your article

### Step 2: Add to Blog Homepage

In `blog.html`, add this at the top of the blog grid:

```html
<article class="blog-card">
    <a href="blog/5-tips-secure-cloud-configuration.html" style="text-decoration: none; color: inherit; display: flex; flex-direction: column; height: 100%;">
        <div class="blog-image">☁️</div>
        <div class="blog-content">
            <div class="blog-meta">
                <span class="blog-date">20 October 2024</span>
                <span class="blog-category">Cloud Security</span>
                <span class="blog-read-time">4 min read</span>
            </div>
            <h3>5 Tips for Secure Cloud Configuration</h3>
            <p class="blog-excerpt">Learn essential security practices for cloud infrastructure to protect your data and applications from potential threats.</p>
            <span class="read-more">Read More →</span>
        </div>
    </a>
</article>
```

Done! Your new blog post is now live.

---

## Blog Post Content Tips

### Good Heading Structure

```html
<h2>Main Section</h2>
<p>Introduction paragraph...</p>

<h3>Subsection</h3>
<p>Details...</p>
```

### Using Lists

```html
<ul>
    <li>Bullet point 1</li>
    <li>Bullet point 2</li>
</ul>

<ol>
    <li>Numbered item 1</li>
    <li>Numbered item 2</li>
</ol>
```

### Highlight Boxes

```html
<div class="highlight-box">
    <strong>Key Takeaway:</strong> Your important message here.
</div>
```

### Inline Code

```html
<code>SELECT * FROM users</code>
```

### Code Blocks

```html
<pre><code>function example() {
    console.log("Hello World");
}</code></pre>
```

---

## Suggested Categories

Choose from these categories (or create your own):

- Penetration Testing
- Red Team
- Security Best Practices
- Vulnerability Research
- Threat Intelligence
- Cloud Security
- Web Security
- Mobile Security
- Network Security
- Incident Response
- Security Training
- Compliance & Regulations

---

## Recommended Emojis for Blog Cards

Match your topic with an appropriate icon:

- 🔒 General Security
- 🎯 Red Team / Targeted Attacks
- ⚡ Fast/Quick Tips
- 🛡️ Defense / Protection
- 🔐 Authentication / Access Control
- 💻 Technical / Development
- 🚀 New Features / Trends
- 📊 Analytics / Reports
- 🌐 Web Security
- ⚔️ Offensive Security
- ☁️ Cloud Security
- 📱 Mobile Security
- 🔍 Analysis / Research

---

## Tips for Great Blog Posts

1. **Write Clear Titles**: Make them specific and action-oriented
2. **Strong Excerpts**: Summarize the value in 2-3 sentences
3. **Scannable Content**: Use headings, lists, and short paragraphs
4. **Add Value**: Share practical insights and actionable advice
5. **Consistent Voice**: Maintain a professional, helpful tone
6. **Call to Action**: End with a way for readers to engage (contact, services, etc.)

---

## Deleting Old Posts

To remove a blog post:

1. Delete the HTML file from the `/blog` folder
2. Remove the corresponding `<article class="blog-card">` section from `blog.html`

---

## Need Help?

If you have questions about:
- HTML formatting
- Styling issues
- Adding images or other media
- Advanced customization

Feel free to reach out or refer to the sample blog post for examples!

---

**Happy Blogging! 📝**
