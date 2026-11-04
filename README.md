# K6 Cast

Landing page for **K6 Cast** – the tech & e-commerce podcast with Samuel and Lucas.

Plain static HTML/CSS, no build step. Everything served lives in `public/`.

## Local preview

```sh
npx serve public
```

## Deploy (Vercel)

1. Import this repo at <https://vercel.com/new> (Framework preset: **Other**, no build command).
   `vercel.json` points the output directory to `public/`.
2. Project → Settings → Domains → add `k6-cast.de` and `www.k6-cast.de`.
3. DNS at your registrar:

| Host               | Type  | Value                  |
|--------------------|-------|------------------------|
| `www.k6-cast.de`   | CNAME | `cname.vercel-dns.com` |
| `k6-cast.de` (apex)| A     | `76.76.21.21`          |

The apex can't be a CNAME, so it uses Vercel's A record. If Vercel's domain page shows a
project-specific value, use that one instead.

## TODO

- Fill in real data in `public/impressum.html` (legally required in Germany)
- Replace placeholder platform links (`href="#"`) once the feed is live
- Replace placeholder episodes and host bios
