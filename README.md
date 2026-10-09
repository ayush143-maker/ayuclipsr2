# ayuclips
Cloudflare-first shared editing workspace starter.

## Cloudflare resources already created
- D1: `ayuclips-db` (ID `66c728ca-75e8-40f3-908f-d5f12939ffa8`)
- Queue: `ayuclips-jobs`
- Dead-letter queue: `ayuclips-jobs-dlq`

R2 is not enabled on the connected Cloudflare account yet. Enable it in Dashboard → R2 Object Storage and create a private bucket named `ayuclips-media`. Then deploy Pages with bindings `DB`, `MEDIA`, `JOBS`; set `WORKSPACE_PASSWORD` and `SESSION_SECRET` as secrets. Run `npx wrangler d1 execute ayuclips-db --remote --file=migrations/0001_initial.sql`.

Important: this is a starter scaffold, not yet an end-to-end video-processing service. Multipart upload and secure output transfer are deliberately marked as incomplete rather than pretending large uploads work. No unlimited free encoding exists.
