# scaffold-pages · minimal static layout (SAMPLE)

This folder is a **documentation scaffold**, not a deployable production app and **not** a Wrangler login guide.

Goal: remind humans (and CI) which knobs Cloudflare Pages cares about for a plain static site.

## Suggested local layout

```text
scaffold-pages/
  README.md          ← you are here
  site/
    index.html       ← tiny placeholder page
    _redirects       ← optional Pages-style redirects note
```

## Pages project settings (checklist teaser)

| Setting | Typical static / Hugo note |
| --- | --- |
| Framework preset | None / Hugo / or custom |
| Build command | empty (prebuilt) **or** `hugo --minify` |
| Build output directory | `.` / `site` for prebuilt · `public` for Hugo |
| Root directory | leave empty unless monorepo |
| Environment variables | never commit secrets; use dashboard encryption |

## What this sample deliberately omits

- No `wrangler` login, no API tokens, no account IDs  
- No paid checklist chapters (DNS pending, cache rules matrix, …)  
- No full Hugo theme  

See repo root `samples/` and Xianyu SKU links in the main README.
