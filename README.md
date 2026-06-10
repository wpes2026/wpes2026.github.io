# WPES 2026 Website

Static website for the **25th Workshop on Privacy in the Electronic Society (WPES 2026)**,
held in conjunction with ACM CCS 2026.

Plain HTML + CSS, no build step. Works on any static host (Vercel, Netlify, GitHub Pages,
or a university web server) — just upload the files.

## Files

```
index.html         Home (scope + key dates)
cfp.html           Call for Papers (topics, submission instructions, dates)
program.html       Program (TBD)
accepted.html      Accepted Papers (TBD)
organization.html  Committees
registration.html  Registration
past.html          Past WPES workshops
css/style.css      Stylesheet (brand color #990000)
img/wpes_logo.png  WPES logo
```

## Preview locally

```bash
cd "WPES 2026"
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to Vercel

**Option A — CLI (fastest):**

```bash
npm i -g vercel        # once
cd "WPES 2026"
vercel                 # deploy a preview; follow the prompts
vercel --prod          # promote to production
```

When asked for settings, accept the defaults — no framework, no build command,
output directory is the project root.

**Option B — Dashboard:** push this folder to a GitHub repo, then import it at
[vercel.com/new](https://vercel.com/new). Vercel auto-detects a static site; click Deploy.

## Migrating to a custom domain later

- **Vercel:** Project → Settings → Domains → add your domain (e.g. a Rutgers
  subdomain) and follow the DNS instructions.
- **University server:** since this is plain static HTML, just copy all files
  (preserving the `css/` and `img/` folders) to the web root. No server-side
  runtime is required.

## TODO before going live

Search the files for `TBD`, `wpes2026@example.org`, and `To be announced`, and fill in:

- [ ] Program Co-Chairs, Publicity Chair, Program Committee (`organization.html`)
- [ ] Location and dates (header subtitle in every page; `index.html`, `cfp.html`)
- [ ] Important dates (`index.html`, `cfp.html`)
- [ ] HotCRP submission link (`cfp.html`)
- [ ] Contact email (footer on every page)
- [ ] Confirm the ACM CCS 2026 URL once published (currently links to the SIGSAC CCS series page)
