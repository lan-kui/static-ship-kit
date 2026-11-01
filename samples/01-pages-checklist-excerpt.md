# SAMPLE · Cloudflare Pages troubleshooting excerpt

> **THIS IS A FREE SAMPLE** — not the full paid checklist.  
> Full product: 闲鱼 SKU3 《Cloudflare Pages 常见报错排错清单》  
> Buy: https://www.goofish.com/item?id=1096814717154 (¥12.9)  
> Excerpt purpose: show the “symptom → where to look” style. Full ZIP adds remaining domains (DNS/cert, cache/redirects, preview vs prod env, capability limits, recording template, etc.).

---

## 0. Symptom jump (abbreviated)

| What you see | Start here (sample) | Full pack section |
| --- | --- | --- |
| Deployments → Build failed / red X | §A below | A. Build & output |
| Build OK but 404 / empty site | §A + think “wrong output dir” | A + B |
| Custom domain cert Pending / red lock | *(paid)* | C. DNS · HTTPS |
| Deployed but still old page | *(paid)* | D. Cache |
| Preview OK, Production broken | *(paid)* | E. Env vars · branch |
| Occasional 502 / 520 / 525 | *(paid)* | C + F |
| Form/API 405 on Pages | *(paid)* | G. Capability boundary |

Rule of thumb: **change one variable at a time**; note time + commit SHA + deploy URL.

---

## A. Build & output directory (partial · SAMPLE)

Only a few starter checks — full SKU3 has the complete checkbox list + framework output table.

- [ ] Open the failed Deployment → **Build log** → read the **last ~30 lines** first  
- [ ] Confirm **Build command** matches local (`npm run build` / `hugo --minify` / `astro build`, …)  
- [ ] Confirm **Build output directory** matches the framework default (`dist` / `public` / `out` / `_site`) — **#1 root cause: pointing at source or leaving it blank**  
- [ ] Monorepo: is **Root directory** set to the real frontend app (e.g. `apps/web`)?  
- [ ] Pin Node (`.nvmrc` / `NODE_VERSION`) so local 20 ≠ remote old default  

**Tiny output cheat-sheet (sample):**

| Framework (examples) | Common output |
| --- | --- |
| Hugo | `public` |
| Astro static | `dist` |
| Vite / many SPAs | `dist` |
| Next static export | `out` (needs correct export config) |

Local reproduce mantra: same command + same Node + same lockfile in a clean directory, then push.

---

## Want the rest?

Paid SKU3 continues with: 404/SPA fallback/base path, DNS & certificates, cache & redirect loops, Preview vs Production env vars, SSL oddities, “Pages ≠ full backend”, and a troubleshooting log template.

→ https://www.goofish.com/item?id=1096814717154

Also useful:

- First-time Hugo × CF production deploy checklist → SKU1 https://www.goofish.com/item?id=1097815676495  
- SEO × Hugo content checklist → SKU2 https://www.goofish.com/item?id=1096750053882  

---

*SAMPLE END · do not treat this file as the complete product.*
