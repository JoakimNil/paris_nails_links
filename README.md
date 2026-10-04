# Paris Nails – links

A one-page link site for Paris Nails, Norheimsund: booking, phone, directions, Instagram, Facebook and Google reviews.

It is a single static `index.html` with no build step.

## Hosting: nails.salongparis.no

The page is published with GitHub Pages and served at **https://nails.salongparis.no**.
`salongparis.no/nails-links` redirects there. salongparis.no itself is a Wix site, and Wix
cannot serve this page at a path, so the subdomain is the real address.

### 1. GitHub: publish the site

1. In this repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
3. Under **Custom domain**, enter `nails.salongparis.no` and save. GitHub reads the `CNAME` file in this
   repository, so the field may already be filled in.
4. Once the DNS record below exists, tick **Enforce HTTPS**. The option appears when GitHub has
   verified the domain, which can take up to an hour after the DNS change.

### 2. Wix: point the subdomain at GitHub

In Wix, open **Settings → Domains → salongparis.no → Manage DNS records** (the wording changes
occasionally; look for DNS or advanced domain settings) and add:

| Type | Host name | Value |
| --- | --- | --- |
| CNAME | `nails` | `joakimnil.github.io` |

Leave everything else as it is. Changes usually take minutes, sometimes a few hours.

### 3. Wix: redirect salongparis.no/nails-links

In the Wix dashboard, open **Marketing & SEO → SEO → URL Redirect Manager** (or search the dashboard
for "redirect") and add a redirect:

- **Old URL:** `/nails-links`
- **New URL:** `https://nails.salongparis.no`

### Changing the address later

If the site moves, update three things: the `CNAME` file, the `og:image` URL in `index.html`
(so link previews on Facebook and Messenger show the image), and the Wix redirect.

## Editing

- **Links, phone and address** are plain `<a href="…">` tags in the `<ul class="links">` list in `index.html`. Each button has a `title` line and an optional smaller `sub` line.
- **Colours** are CSS variables at the top of the `<style>` block (`--blush`, `--pill`, `--line`, …).
- **Spacing between buttons** is the `--gap` variable.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The page |
| `assets/logo.png`, `assets/logo.webp` | Logo with a transparent background |
| `assets/og-image.png` | Preview image when the link is shared |
| `assets/favicon.svg`, `assets/apple-touch-icon.png` | Browser tab and home-screen icons |
| `CNAME` | Custom domain for GitHub Pages |
