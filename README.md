# ZeroDay Society

A modern, professional cybersecurity research blog focused on vulnerability analysis, threat intelligence, and security insights.

![ZeroDay Society](https://img.shields.io/badge/Security-Research-00d4ff?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-10b981?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-7c3aed?style=for-the-badge)

## 🎯 Overview

ZeroDay Society is a cybersecurity blog platform designed to share in-depth analysis of:
- Vulnerability research and findings
- Security research paper reviews
- Industry gap analysis
- Mitigation strategies and best practices
- Threat intelligence insights

## ✨ Features

- **Modern Dark Theme**: Cybersecurity-focused design with gradient accents
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Fast & Lightweight**: Pure HTML/CSS/JavaScript with no framework dependencies
- **SEO Optimized**: Meta tags and semantic HTML for better discoverability
- **Accessible**: WCAG compliant with proper heading structure and ARIA labels
- **GitHub Pages Ready**: Deploy in minutes with GitHub Pages

## 🚀 Quick Start

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/zeroday-society.git
   cd zeroday-society
   ```

2. **Open in browser**
   - Simply open `index.html` in your web browser
   - Or use a local development server:
   
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```

3. **View the site**
   - Open `http://localhost:8000` in your browser

## 📦 Deployment to GitHub Pages

### Method 1: Using GitHub Pages Settings (Recommended)

1. **Create a new repository on GitHub**
   - Go to https://github.com/new
   - Name it `zeroday-society` (or any name you prefer)
   - Keep it public (required for free GitHub Pages)
   - Don't initialize with README (you already have one)

2. **Push your code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: ZeroDay Society blog"
   git branch -M main
   git remote add origin https://github.com/yourusername/zeroday-society.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** > **Pages**
   - Under "Source", select **Deploy from a branch**
   - Select branch: **main** and folder: **/ (root)**
   - Click **Save**

4. **Access your site**
   - Your site will be available at: `https://yourusername.github.io/zeroday-society/`
   - It may take a few minutes for the site to go live

### Method 2: Custom Domain (Optional)

If you want to use a custom domain like `zerodaysociety.com`:

1. **Add a CNAME file**
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. **Configure DNS**
   - Add an `A` record pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Or add a `CNAME` record pointing to `yourusername.github.io`

3. **Update GitHub Settings**
   - Go to Settings > Pages
   - Enter your custom domain
   - Enable "Enforce HTTPS"

## 📁 Project Structure

```
zeroday-society/
│
├── index.html              # Homepage
├── css/
│   └── style.css          # Main stylesheet
├── js/
│   └── main.js            # JavaScript functionality
├── posts/                 # Blog posts
│   ├── supply-chain-attacks.html
│   ├── zero-trust-architecture.html
│   └── ...
├── README.md              # This file
└── CNAME                  # Custom domain (optional)
```

## ✍️ Adding New Blog Posts

1. **Create a new HTML file** in the `posts/` directory
   ```bash
   cp posts/supply-chain-attacks.html posts/your-new-post.html
   ```

2. **Edit the content**
   - Update the `<title>` and meta tags
   - Change the post header (tag, title, date)
   - Replace the article content
   - Update related posts section

3. **Add to homepage**
   - Open `index.html`
   - Add a new post card in the posts section:
   
   ```html
   <article class="post-card">
       <div class="post-tag">Your Category</div>
       <h3 class="post-title">
           <a href="posts/your-new-post.html">Your Post Title</a>
       </h3>
       <p class="post-excerpt">
           Brief description of your post...
       </p>
       <div class="post-meta">
           <span class="post-date">December 1, 2025</span>
           <span class="post-reading-time">5 min read</span>
       </div>
       <a href="posts/your-new-post.html" class="post-link">Read Analysis →</a>
   </article>
   ```

4. **Commit and push**
   ```bash
   git add .
   git commit -m "Add new post: Your Post Title"
   git push
   ```

## 🎨 Customization

### Colors

Edit the CSS variables in `css/style.css`:

```css
:root {
    --bg-primary: #0a0e17;        /* Main background */
    --bg-secondary: #131824;       /* Section backgrounds */
    --accent-primary: #00d4ff;     /* Primary accent color */
    --accent-secondary: #7c3aed;   /* Secondary accent color */
    /* ... more variables ... */
}
```

### Fonts

The site uses:
- **Inter** for body text (clean, modern)
- **Fira Code** for code blocks (monospace)

To change fonts, update the Google Fonts import in HTML files:

```html
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@400;500;700&display=swap" rel="stylesheet">
```

### Logo

Update the logo text in the navigation:

```html
<a href="index.html" class="logo">
    <span class="logo-bracket">[</span>
    <span class="logo-text">Your Blog Name</span>
    <span class="logo-bracket">]</span>
</a>
```

## 🔧 Configuration

### Analytics (Optional)

To add Google Analytics, insert this before the closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Newsletter Integration

The newsletter form currently shows a notification. To integrate with a real service:

1. **Mailchimp**: Replace the form with Mailchimp's embedded form code
2. **ConvertKit**: Use ConvertKit's form HTML
3. **Custom Backend**: Update the JavaScript in `js/main.js` to POST to your API

Example:
```javascript
newsletterForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    const email = newsletterForm.querySelector('input[type="email"]').value;
    
    try {
        const response = await fetch('YOUR_API_ENDPOINT', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify({ email })
        });
        
        if (response.ok) {
            showNotification('Thanks for subscribing! 🎉', 'success');
            newsletterForm.reset();
        }
    } catch (error) {
        showNotification('Subscription failed. Please try again.', 'error');
    }
});
```

## 🔒 Security Considerations

- All external links should use `rel="noopener noreferrer"`
- Implement Content Security Policy (CSP) headers
- Use HTTPS for custom domains
- Regularly update dependencies
- Sanitize any user-generated content

## 📱 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Android)

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Web.dev Best Practices](https://web.dev/)
- [MDN Web Docs](https://developer.mozilla.org/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

## 💡 Tips for Success

1. **Write Quality Content**: Focus on providing valuable insights and analysis
2. **SEO Optimization**: Use descriptive titles, meta descriptions, and proper heading structure
3. **Regular Updates**: Post consistently to build an audience
4. **Engage with Community**: Share your posts on social media and security forums
5. **Mobile First**: Test on mobile devices regularly
6. **Performance**: Keep images optimized and minimize external dependencies
7. **Accessibility**: Ensure content is accessible to all users

## 🐛 Troubleshooting

### Site not updating after push?
- Clear your browser cache
- Check GitHub Pages build status in repository settings
- Wait 1-2 minutes for changes to propagate

### Broken links or missing styles?
- Ensure file paths are correct (case-sensitive)
- Check that all files are committed and pushed
- Verify CSS/JS files are in correct directories

### Custom domain not working?
- Verify DNS records are properly configured
- Wait up to 24 hours for DNS propagation
- Check GitHub Pages settings

## 📧 Contact

For questions or support, open an issue on GitHub or contact through:
- GitHub Issues: [Your Repository URL]
- Twitter: [@yourusername]
- Email: your.email@example.com

---

**Built with 💙 for the cybersecurity community**

*"Knowledge shared is security multiplied"*

