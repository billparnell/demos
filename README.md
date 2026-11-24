# demos

Design mockups and one-off demos. Each project folder has its own BRIEF / DESIGN / BACKLOG.
The repo is private; only `public/` is ever served.

- `lilis-brazilian/` — vibrant Brazilian homepage mockup for Lili's Brazilian Steakhouse (Chico). Start at its BACKLOG.md. (Claude design canvas, not in `public/`.)
- `healthysteps-maryjo/` — one-page site demo for Mary Jo Brown's Healthy Steps classes (Chico). Page is `public/healthysteps/`.

## Sharing a demo at demos.parnellprojects.com

Everything in `public/` is published by a Cloudflare Worker (static assets, no server,
free) on every push to `main`. Config is `wrangler.jsonc` at the repo root.

**To add a demo:** make a folder `public/<name>/` with an `index.html` (a full HTML doc:
doctype, `<head>`, `<body>`) and its images beside it. Push. It shows up at
`https://demos.parnellprojects.com/<name>/` about a minute later.

- Every page is `noindex` (via `public/_headers`), so demos of real businesses stay out of Google.
- The bare domain shows a one-line "nothing here" page on purpose: people only see the link you send them.
- Don't put anything in `public/` you wouldn't want a stranger with the link to see.

**One-time Cloudflare setup** (PLAYBOOK §9 has the gotchas):
1. Cloudflare dashboard → **Workers & Pages → Create → Import a repository** → GitHub →
   allow **only** `billparnell/demos` → select it.
2. Framework preset **None**, build command **empty**, deploy command default
   (`npx wrangler deploy`), **root directory `/`**. Save and Deploy.
3. The `demos` worker → **Settings → Domains & Routes → Add → Custom domain** → pick zone
   `parnellprojects.com` from the list, then `demos`. Never click "Onboard domain".
