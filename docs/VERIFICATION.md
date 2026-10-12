# Verification record — 2026-10-12

## Completed locally

- Copied all ten approved PNGs, the approved contact sheet, and the brand reference without changing bytes.
- SHA-256 checks match every supplied source. The existing repository avatar matches the supplied 400px avatar exactly and was not replaced.
- PNG chunk CRCs and compressed data validated for ten originals plus one new proposal. The three transparent originals retain RGBA headers and exact source bytes.
- Inspected the supplied contact sheet, community banner, and recovered chat screenshots. The visible Discord direct-upload banner matches the community banner composition. No distinct welcome-banner source file was available.
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

An owner-authorized Carl-bot sandbox test in desktop Discord is still required to determine whether the hosting change resolves the embed symptom. The proposed announcement background requires owner review before use. No additional approved welcome-banner source beyond the matching community banner was available in the project.

Efrotz HQ, Carl-bot configuration, and social content were not changed. No Discord test messages were sent.
