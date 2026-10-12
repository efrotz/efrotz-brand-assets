# GitHub Pages and Discord image hosting

## Publishing source

Configured on 2026-10-12: **Settings → Pages → Deploy from a branch → main → / (root)**. HTTPS is enforced on the default domain. The root `.nojekyll` and `index.html` provide static serving. No custom domain is configured.

GitHub reference: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Verified direct image URLs

- Avatar: `https://efrotz.github.io/efrotz-brand-assets/approved/avatars/efrotz-avatar-400.png`
- Community/welcome banner: `https://efrotz.github.io/efrotz-brand-assets/approved/banners/efrotz-community-banner.png`
- Index: `https://efrotz.github.io/efrotz-brand-assets/`

These paths returned HTTP 200 after successful deployment on 2026-10-12. The PNGs were served as `image/png` and matched the approved source checksums. See `VERIFICATION.md` for results. Desktop Discord embed behavior has not yet been tested.

## Carl-bot check after hosting is live

Use the direct `.png` banner URL in the embed's image field and the avatar URL in the thumbnail field. Do not use a GitHub `blob` page, the asset index, or an image-hosting landing page as an image URL.

1. Confirm anonymous GET returns HTTP 200 with `Content-Type: image/png`, a decodable PNG, and the expected checksum.
2. Open the direct URLs in a browser and confirm the images render.
3. In an owner-authorized sandbox, replace the existing image URLs and trigger a new Carl-bot preview/test greeting.
4. Inspect that new message in desktop Discord. Compare with a direct upload. If it still fails, check embed fields, Discord media settings, and proxy/cache behavior.

No Carl-bot setting, Discord server, or Efrotz HQ change was made during this asset publication. Serving valid PNGs is necessary but does not prove that Discord's proxy will render an embed. The earlier screenshot shows successful direct uploads and a blank embed; it does not establish the exact cause of the postimg failure.

## Updating assets

Keep existing URLs stable. Add versioned siblings for revisions and retain originals. Do not point production embeds at `proposed/`. Original-name mapping and checksums are recorded in `asset-inventory.json`.
