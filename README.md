# Mubarek Bora — Portfolio

Personal portfolio site, built on the purchased "MyBio" one-page ThemeForest template (Bootstrap 3, jQuery). No build step -- plain HTML/CSS/JS.

**Live:** https://mubarek-boraportifolio.netlify.app

## Structure

- `html/` — the site itself; this is the Netlify publish directory (see `netlify.toml`)
  - `index.html` — Hero, About, Work Experience/Education, Portfolio, Skills, Contact
  - `css/custom.css` — overrides/additions layered on top of the vendor `style.css` (text logo, avatar, portfolio tiles, static hero background)
  - Only the template sections that fit a personal dev portfolio are used. The original template also ships Services, Testimonials, Client logos, Pricing, Blog, and FAQ sections (see `elements.html` in the original zip under `Documentation/` if you ever want to reintroduce one) -- dropped here since they'd need fabricated content (fake testimonials, fake clients, pricing tiers) to fill in.
  - The Portfolio section is a plain grid, not the template's original owl-carousel/filter setup -- project categories (WordPress/Magento/etc.) didn't apply, and the projects don't have real screenshots, so each card shows a colored initials tile instead of an image.
  - The Contact form uses Netlify Forms (`data-netlify="true"` + honeypot field) instead of the template's original PHP handler, since Netlify doesn't run PHP.
- `Documentation/`, `psd/` — leftover assets from the original ThemeForest template purchase; unused, kept for reference

## Updating

Edit `html/index.html` (projects, bio, experience) or `html/css/custom.css`, then commit and push. Once this repo is connected to the Netlify site (Site settings → Build & deploy → Connect to repository), every push to `main` deploys automatically.
