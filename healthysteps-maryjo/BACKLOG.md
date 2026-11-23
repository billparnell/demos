# Healthy Steps demo — backlog

## Where we are (handoff, 2026-11-23)
- Demo v1 published: https://claude.ai/artifact/2vBNg5istCQUc7pewxpqFa (private; share from its Share menu).
- Photos are from her current site; the "Recent photos" section is the slot for Facebook photos.
- **Not yet checked at 375px in a real browser** — Chrome extension wasn't connected.
- Next task: top unchecked item.

## Phase 1: Demo
- [x] Pull copy, classes, testimonials, photos from healthysteps-maryjo.com
- [x] Build and publish the one-pager (no newsletter, no blog)
- [ ] Check at 375px in Chrome (header wrap, class card dl rows, contact email length)
- [ ] Swap gallery (and maybe hero) for recent Facebook photos once we have them
- [ ] Bill/Mary Jo review → cosmetic iteration; answer open questions in BRIEF.md

## Facebook photo options
1. **She sends them** (text/email/shared Google Photos album). Fastest, best quality, no tech. Recommended for the demo.
2. **Bill grabs them in his own browser** from her page's Photos tab (needs the Chrome extension connected). Fine for a demo; fbcdn URLs expire, so download and host copies.
3. **Live feed on the real site**: Facebook Page Plugin embed (shows recent posts; heavy, cookie banner, looks like Facebook), or Graph API with a Page token she grants (auto-pulls photos; needs a Meta app + token refresh — overkill unless she posts constantly).

## Log
- **2026-11-23**: Scraped site, built and published v1. Facebook blocks scripted fetches (HTTP 400), Chrome extension not connected, so FB photos are pending.
