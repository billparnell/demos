# Healthy Steps demo — backlog

## Where we are (handoff, 2026-11-23)
- Page lives at `public/healthysteps/` and will serve at https://demos.parnellprojects.com/healthysteps/
  once Bill pushes and does the one-time Cloudflare setup (see repo README).
- Photos are from her current site; the "Recent photos" section is the slot for Facebook photos.
- Checked at 375px with headless Chrome in a 375px iframe (2026-11-24). Chrome extension still not connected.
- Next task: top unchecked item.

## Phase 1: Demo
- [x] Pull copy, classes, testimonials, photos from healthysteps-maryjo.com
- [x] Build and publish the one-pager (no newsletter, no blog)
- [x] Check at 375px (fixed stretched photos; everything else fits)
- [x] Move to `public/healthysteps/` for demos.parnellprojects.com
- [ ] Bill: push + Cloudflare setup, then confirm the live URL on the iPhone
- [ ] Swap gallery (and maybe hero) for recent Facebook photos once we have them
- [ ] Bill/Mary Jo review → cosmetic iteration; answer open questions in BRIEF.md

## Facebook photo options
1. **She sends them** (text/email/shared Google Photos album). Fastest, best quality, no tech. Recommended for the demo.
2. **Bill grabs them in his own browser** from her page's Photos tab (needs the Chrome extension connected). Fine for a demo; fbcdn URLs expire, so download and host copies.
3. **Live feed on the real site**: Facebook Page Plugin embed (shows recent posts; heavy, cookie banner, looks like Facebook), or Graph API with a Page token she grants (auto-pulls photos; needs a Meta app + token refresh — overkill unless she posts constantly).

## Log
- **2026-11-24**: Moved page to `public/healthysteps/`, made it a standalone HTML doc, fixed photos stretching tall on phones (`height:auto`). Photos now committed.
- **2026-11-23**: Scraped site, built and published v1. Facebook blocks scripted fetches (HTTP 400), Chrome extension not connected, so FB photos are pending.
