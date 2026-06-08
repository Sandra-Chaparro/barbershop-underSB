
## Features

- **Zero Dependencies** - Only Astro, no Tailwind CSS, no UI frameworks, no bloat
- **Ultra Lightweight** - Pure CSS styling, minimal vanilla JS, blazing fast load times
- **Vintage/Industrial Aesthetic** - Deep charcoal backgrounds, aged brass accents, elegant typography
- **JSON-based CMS** - All content managed through a single `site.json` file
- **Fully Responsive** - Mobile-first design with desktop, tablet, and mobile breakpoints
- **SEO Optimized** - Meta tags, Open Graph, Twitter Cards, and LocalBusiness structured data
- **Accessible** - Semantic HTML, ARIA labels, keyboard navigation, high contrast ratios
- **Performance First** - Lazy-loaded images, minimal JavaScript, optimized fonts
- **Interactive Components** - Accordion menus, lightbox gallery with keyboard support
- **Article Pages** - Built-in blog/article system with list and detail pages

### Why No Third-Party Dependencies?

This theme intentionally uses **only Astro** as its dependency:

| What We Don't Use | Why |
|-------------------|-----|
| Tailwind CSS | Pure CSS with custom properties is lighter and more maintainable |
| React/Vue/Svelte | Static site doesn't need client-side frameworks |
| UI Component Libraries | Custom components are leaner and fully customizable |
| Animation Libraries | CSS animations handle everything we need |
| Lightbox Libraries | ~50 lines of vanilla JS does the job |

### Social Media

```json
{
  "social": {
    "instagram": "https://instagram.com/youracct"
  }
}
```

### SEO Settings

```json
{
  "seo": {
    "metaTitle": "Your Bar Name | Neighborhood Bar in City",
    "metaDescription": "A warm neighborhood bar serving craft beers and cocktails at 123 Main Street."
  }
}

### Robots.txt

The `public/robots.txt` file controls search engine crawling. By default, all crawlers are allowed:

```txt
User-agent: *
Allow: /
```

To add a sitemap, uncomment and update the Sitemap line with your domain:

```txt
Sitemap: https://yourdomain.com/sitemap.xml
```
## Deployment

### Build for Production

```bash
npm run build
```

This creates an optimized static site in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

### Deploy Options

#### Option 1: One-Click Deploy (Recommended)

Use the deploy buttons at the top of this README to instantly deploy to:
- **Netlify** - Free tier available, automatic HTTPS
- **Vercel** - Free tier available, great performance
- **Cloudflare Pages** - Free tier available, global CDN

#### Option 2: Manual Deploy

**Netlify:**
1. Push your code to GitHub
2. Connect your repo to [Netlify](https://netlify.com)
3. Build command: `npm run build`
4. Publish directory: `dist`

**Vercel:**
1. Push your code to GitHub
2. Import your repo on [Vercel](https://vercel.com)
3. Vercel auto-detects Astro settings

**Cloudflare Pages:**
1. Push your code to GitHub
2. Connect your repo to [Cloudflare Pages](https://pages.cloudflare.com)
3. Build command: `npm run build`
4. Build output directory: `dist`

#### Option 3: Self-Hosted / VPS

1. Build the site: `npm run build`
2. Upload the `dist/` folder to your server
3. Configure your web server (Nginx, Apache) to serve static files

**Nginx example:**

```nginx
server {
    listen 80;
    server_name yourbar.com;
    root /var/www/quiet-bar/dist;
    index index.html;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
}
```

## Commands Reference

| Command | Description |
|---------|-------------|
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build for production to `./dist/` |
| `npm run preview` | Preview production build locally |

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - Feel free to use this template for personal or commercial projects.

## Support

Need help? [Open an issue](https://github.com/larry-xue/quiet-bar/issues) on GitHub or [contact the creator](https://larryxue.dev/contact) for professional support.
