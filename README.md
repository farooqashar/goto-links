# goto-links

Personal short links at **goto.asharfarooq.xyz**, e.g. `goto.asharfarooq.xyz/linkedin`.

It's just a [`vercel.json`](./vercel.json) of redirects, deployed on Vercel. There's no app and no build step.

## Links

| Path | Goes to |
| --- | --- |
| `/linkedin`, `/li` | LinkedIn |
| `/github`, `/gh` | GitHub |
| `/x`, `/twitter` | X / Twitter |
| `/instagram`, `/ig` | Instagram |
| `/facebook`, `/fb` | Facebook |
| `/calendly`, `/meet` | Calendly |
| `/resume` | Résumé PDF |
| `/site` | ashar.vercel.app |
| `/ai`, `/reading`, `/tools` | Side sites |
| `/` and anything unknown | ashar.vercel.app |

## Adding a link

Add a line to `redirects` in `vercel.json` **above the final `/:path*` catch-all** (rules match top to bottom), then push. Vercel redeploys automatically.

```json
{ "source": "/newthing", "destination": "https://example.com", "permanent": false }
```

Keep `"permanent": false` (307). Browsers cache 301s aggressively, so changing a permanent link later wouldn't reach people who already clicked it.

## Setup

1. Import this repo in Vercel (Framework preset: **Other**, no build command).
2. Project → Settings → Domains → add `goto.asharfarooq.xyz`.
3. At Gen.xyz DNS, add a **CNAME**: host `goto` → `cname.vercel-dns.com`.

> Note: asharfarooq.xyz lapses around April 2027. After that these links stop working, so use the real URLs anywhere that needs to last.
