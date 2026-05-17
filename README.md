# nextjs-app-deplyment-checklist

#### the things to check before flipping the DNS
- Tests are green
- Protected URLs are set (optimistic check in `proxy.ts`)
- CSP, X-Frame-Options, Strict-Transport-Security in `proxy.ts` or `next.config.ts`
- No heavy compute in `proxy.ts`
- Telemetry: error tracking, logging
- `not-found.tsx`, `error.tsx`, `global-error.tsx` defined
- cache strategy: `force-dynamic`, ISR with `revalidate` or static
- OpenGraph images verified in the Twitter/Facebook debuggers
- SEO: sitemap submitted to the GSC
- Rate limiting on Server Functions
- next/image `remotePatterns` configured
- `@next/bundle-analyzer`
- database migration plan
