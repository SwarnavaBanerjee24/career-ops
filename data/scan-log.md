# Scan Log

## 2026-06-23 — FAILED (network egress blocked)

**Result:** 0 companies scanned, 0 new jobs found
**Reason:** HTTP 403 — hosts not in egress allowlist

### Blocked hosts

| Host | Companies affected |
|------|-----------------|
| `boards-api.greenhouse.io` | Celonis, Helsing, Black Forest Labs, Aleph Alpha, N26, Trade Republic, SumUp, HelloFresh, GetYourGuide, Contentful, Siemens Energy, and more |
| `api.ashbyhq.com` | ElevenLabs, n8n, Zapier, Vapi, Sierra, Cohere, DeepL, Synthesia, Perplexity, Supabase, WorkOS, Resend, Clerk, and more |
| `api.lever.co` | Mistral AI, Palantir, Qonto, Forto, Vinted, Spotify, Clarity AI |
| `api.smartrecruiters.com` | Siemens Energy, Syntegon |
| `apply.workable.com` | Hugging Face, Semios |

56 additional companies (HENSOLDT, Knorr-Bremse, Rohde & Schwarz, Infineon, MTU, Bertrandt, Vector Informatik, MAHLE, DEKRA, Dräger, ...) require WebSearch which is also unavailable under the current egress policy.

### How to fix

In your Claude Code on the web environment settings, add these hosts to the network egress allowlist:

```
boards-api.greenhouse.io
api.ashbyhq.com
api.lever.co
api.smartrecruiters.com
apply.workable.com
```

See: https://code.claude.com/docs/en/claude-code-on-the-web

### State

- `data/scan-history.tsv` — unchanged, no drift
- `data/new-jobs.md` — unchanged, no false entries
