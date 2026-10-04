# Paris Nails – links

A one-page link site for Paris Nails, Norheimsund: booking, phone, directions, Instagram, Facebook and Google reviews.

It is a single static `index.html` with no build step.

## Publish with GitHub Pages

1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, pick the branch and `/ (root)`, and save.
3. The site appears at `https://joakimnil.github.io/paris_nails_links/` after a minute or two.

If the site ends up at a different address (for example a custom domain), update the `og:image` URL in `index.html` so link previews on Facebook and Messenger show the image.

## Editing

- **Links, phone and address** are plain `<a href="…">` tags in the `<ul class="links">` list in `index.html`. Each button has a `title` line and an optional smaller `sub` line.
- **Colours** are CSS variables at the top of the `<style>` block (`--blush`, `--pill`, `--line`, …).
- **Spacing between buttons** is the `--gap` variable.
- **The rose spray** is `assets/spray.svg`, drawn as gold ink on the page colour. Its size and position are set in the `.spray` rules; on wide screens a mirrored copy sits in the top-left corner.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The page |
| `assets/logo.png`, `assets/logo.webp` | Logo with a transparent background |
| `assets/spray.svg` | Fine-line rose spray used as the corner decoration |
| `assets/og-image.png` | Preview image when the link is shared |
| `assets/favicon.svg`, `assets/apple-touch-icon.png` | Browser tab and home-screen icons |
