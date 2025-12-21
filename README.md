# Wedding Website

A lightweight, mobile-first wedding website built with plain HTML and CSS. Designed to be hosted on GitHub Pages.

## Quick Start

### Run Locally

Simply open `index.html` in your browser:

```bash
# Or use a local server (optional, for testing)
python -m http.server 8000
# Then visit http://localhost:8000
```

### Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push all files to the `main` branch
3. Go to **Settings > Pages**
4. Under "Source", select `main` branch and `/ (root)` folder
5. Click Save
6. Your site will be live at `https://yourusername.github.io/repository-name/`

**Tip:** For a cleaner URL, name your repo `yourusername.github.io` to get `https://yourusername.github.io/`

## Updating Content

### Key Placeholders to Replace

Search for these placeholders across all HTML files and replace with your actual content:

| Placeholder | Description | Files |
|-------------|-------------|-------|
| `[[DATE]]` | Wedding date | index.html, schedule/index.html |
| `[[TOWN, STATE]]` | Location | index.html, travel/index.html |
| `[[VENUE_NAME]]` | Venue name | schedule/index.html |
| `[[VENUE_ADDRESS]]` | Full address | schedule/index.html |
| `[[RSVP_DEADLINE]]` | RSVP deadline | index.html, rsvp/index.html |
| `[[CONTACT_EMAIL]]` | Contact email | All pages (footer), rsvp/index.html, faq/index.html |
| `[[GOOGLE_FORM_EMBED_URL]]` | Google Form URL | rsvp/index.html |
| `[[REGISTRY_URL]]` | Registry link | registry/index.html |
| `[[DONATION_URL]]` | Cash fund link | registry/index.html |

### Adding the Google Form

1. Create your RSVP form in Google Forms
2. Click "Send" > embed icon (`<>`)
3. Copy the `src` URL from the iframe code
4. Open `rsvp/index.html`
5. Find `<!-- TODO: paste Google Form embed link -->` and replace with your URL

### Editing Page Content

Each page is a standalone HTML file:

- `index.html` — Home page
- `schedule/index.html` — Schedule & events
- `travel/index.html` — Travel & lodging info
- `things-to-do/index.html` — Local activities
- `rsvp/index.html` — RSVP form
- `registry/index.html` — Gift registry
- `faq/index.html` — FAQ

### Styling

All styles are in `css/styles.css`. The color scheme uses CSS variables at the top of the file for easy customization.

## File Structure

```
wedding_site/
├── index.html              # Home page
├── css/
│   └── styles.css          # All styles
├── schedule/
│   └── index.html
├── travel/
│   └── index.html
├── things-to-do/
│   └── index.html
├── rsvp/
│   └── index.html
├── registry/
│   └── index.html
├── faq/
│   └── index.html
└── README.md
```

## Optional: Privacy / Password Protection

If you'd like to add a simple password gate to keep the site semi-private:

### Option 1: Simple JavaScript Password (Low Security)
Add a JavaScript prompt that checks a password before showing content. This is **not secure** (password visible in source code) but deters casual browsing.

### Option 2: Unlisted + Robots.txt
Keep the site unlisted (don't share the URL publicly) and add a `robots.txt` to discourage search engine indexing:

```txt
User-agent: *
Disallow: /
```

### Option 3: Private Repository
Use GitHub Pages with a private repository (requires GitHub Pro/Teams).

### Option 4: Third-Party Services
Use services like Cloudflare Access or Netlify Password Protection for real authentication.

**Current approach:** The site is public but unlisted. Only share the URL via your wedding invitations.

## Tips

- **QR Codes:** Generate a QR code pointing to your site URL for paper invitations
- **Short URLs:** Consider a custom domain or URL shortener for easy typing
- **Mobile Testing:** Test on actual phones, not just browser dev tools
- **Updates:** The "Last updated" date in the footer helps guests know if content changed

## License

This template is free to use for personal wedding websites.
