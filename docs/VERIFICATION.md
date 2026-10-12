# Verification record — 2026-10-12

## Completed locally

- Copied all ten approved PNGs, the approved contact sheet, and the brand reference without changing bytes.
- SHA-256 checks match every supplied source. The existing repository avatar matches the supplied 400px avatar exactly and was not replaced.
- PNG chunk CRCs and compressed data validated for ten originals plus one new proposal. The three transparent originals retain RGBA headers and exact source bytes.
- Inspected the supplied contact sheet, community banner, and recovered chat screenshots. The visible Discord direct-upload banner matches the community banner composition. A separate custom 'Welcome to Efrotz HQ' banner from the Discord setup has since been added as a hosted 1280px export; its full-resolution 2172x724 original remains in the ChatGPT conversation.
- All local index links resolve; all ten approved PNGs load in the browser with expected native dimensions. Layout visually inspected.
- One generated background is explicitly labeled proposed/unapproved, including the exact prompt and noted tonal variation. Palette CSS/JSON retain the four exact locked hex values.

## Live URL results

Anonymous HTTP GET checks:

| URL | Result |
|---|---|
| https://raw.githubusercontent.com/efrotz/efrotz-brand-assets/main/approved/avatars/efrotz-avatar-400.png | 200, image/png; SHA-256 matches approved avatar |
| https://efrotz.github.io/efrotz-brand-assets/ | 200, live asset library |
| https://efrotz.github.io/efrotz-brand-assets/approved/avatars/efrotz-avatar-400.png | 200, image/png; checksum matches |
| https://efrotz.github.io/efrotz-brand-assets/approved/banners/efrotz-community-banner.png | 200, image/png; checksum matches |

All 13 inventory entries were fetched anonymously from Pages and matched their SHA-256 checksums. Every PNG returned `image/png`. All ten approved images rendered in the live browser index. The uploaded remote Git blobs also match all 13 inventory checksums.

The user authenticated the repository-owner browser session, resolving the initial CLI access limitation. Files were uploaded and committed through GitHub's web interface. GitHub Pages was enabled from `main` / root with HTTPS enforced. Initial deployment [38297184904](https://github.com/efrotz/efrotz-brand-assets/actions/runs/38297184904) completed successfully.

## Remaining

An owner-authorized Carl-bot sandbox test in desktop Discord is still required to determine whether the hosting change resolves the embed symptom. The proposed announcement background requires owner review before use. The custom Welcome to Efrotz HQ banner is now in approved/discord/ as a 1280px hosting export. The original full-size PNG was not imported.

Efrotz HQ, Carl-bot configuration, and social content were not changed. No Discord test messages were sent.

## Additional approved Discord graphics — 2026-10-12

A one-time GitHub Action imported and verified two approved images previously used in Carl-bot:

- `approved/discord/efrotz-welcome-mascot-512.png` — original 512 × 512 PNG exactly preserved; SHA-256 `d130e7bd82806b84c68fdcf7ab6f06180dc0aac52839420b45b24838fae052c8`.
- `approved/discord/efrotz-welcome-banner-1280.png` — approved custom wide banner, 1280 × 427 PNG as returned by the original Postimages link; SHA-256 `10cdb9600f577d4541557fc8bfef27ed5fa38d92e14ccb9b6e40df76eff3ff57`. Postimages resized the original 2172 × 724 artwork; this version is not a byte-identical or full-resolution source master.

The verified import completed successfully in [run 38298995400](https://github.com/efrotz/efrotz-brand-assets/actions/runs/38298995400). The updated public asset-library Pages deployment completed successfully in [run 38299199600](https://github.com/efrotz/efrotz-brand-assets/actions/runs/38299199600). The exact hosted links are listed in [HOSTING.md](HOSTING.md).

The user's first GitHub Pages avatar thumbnail worked in desktop Carl-bot, supporting the hosting fix. The newly uploaded 512px thumbnail and custom 1280px banner still require a separate desktop Discord render test before their Carl-bot configuration can be called verified.
