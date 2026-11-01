# SAMPLE · Hugo launch ideas (short)

> **THIS IS A FREE SAMPLE** — not the full paid Hugo × Cloudflare production checklist.  
> Full product: 闲鱼 SKU1 《Hugo × Cloudflare 静态站生产部署 Checklist》  
> Buy: https://www.goofish.com/item?id=1097815676495 (¥9.9)  
> Style only: a few reminders you can paste into your own runbook.

---

## Before you connect Pages

- [ ] `baseURL` in `hugo.toml` / `config.yaml` matches the **final** public domain (or Preview URL while testing)  
- [ ] `hugo server` and `hugo --minify` both succeed locally  
- [ ] Pin Hugo version in CI / Pages so “works on my laptop” ≠ broken remote  
- [ ] Do **not** commit generated `public/` — let Pages/CI build it  
- [ ] Compress large content images early (LCP killers on content sites)

## Pages binding (teaser)

- [ ] Production branch is the one you think it is (`main` / `master`)  
- [ ] Build command + **output directory `public`** match Hugo  
- [ ] Secrets never go into the frontend bundle; use Workers / server-side if needed  
- [ ] Prefer Preview deploy review before promoting to Production  

## After first HTTPS success (teaser)

- [ ] One canonical host: apex **or** `www`, not both fighting  
- [ ] `robots.txt` / `sitemap.xml` reachable on the canonical host  
- [ ] Record: time · commit SHA · deploy URL · how to roll back one click  

---

## Full pack difference

Paid SKU1 expands into printable sections: repo/build, CF Pages hosting, DNS/HTTPS/cache, optional forms/search/comments, observability/rollback, content-site SEO notes, launch-day 30-minute smoke test, and content-site (BreedPedia-class) footnotes.

→ https://www.goofish.com/item?id=1097815676495

If the site already deploys but fails oddly, prefer **SKU3** troubleshooting pack:  
https://www.goofish.com/item?id=1096814717154

---

*SAMPLE END*
