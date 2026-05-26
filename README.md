# Infobase Documentation

OneInbox Infobase guide — powered by [Mintlify](https://mintlify.com).

## Live sites

| URL | How it works |
|-----|----------------|
| [oneinbox.mintlify.app](https://oneinbox.mintlify.app) | Mintlify hosting (source of truth) |
| [infobase-docs.vercel.app](https://infobase-docs.vercel.app) | Vercel proxy → Mintlify |

## Local preview

```bash
npm i -g mint
mint dev
```

## Deploy to Mintlify

Push to [jagriti-sh11/docs](https://github.com/jagriti-sh11/docs) on `main`. Mintlify deploys automatically when the GitHub App is connected.

## Deploy to Vercel (proxy)

This project uses [Vercel rewrites](https://www.mintlify.com/docs/deploy/vercel) to proxy to `oneinbox.mintlify.app` — no static export build.

```bash
vercel deploy --prod
```

### Host on your main domain at `/docs`

1. In [Mintlify → Custom domain](https://dashboard.mintlify.com/settings/deployment/custom-domain), turn on **Host at `/docs`**.
2. Add your domain (e.g. `oneinbox.ai`).
3. Merge `vercel.docs-subpath.json` rewrites into your main site's `vercel.json` (see [Mintlify Vercel guide](https://www.mintlify.com/docs/deploy/vercel)).
