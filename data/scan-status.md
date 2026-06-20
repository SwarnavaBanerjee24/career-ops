# Scan Status Log

## 2026-06-20 — BLOCKED (network egress)

The scheduled scan could not retrieve any jobs. The remote execution environment's network egress policy blocked all outbound requests to career portal APIs.

**Blocked hosts:**

| Host | Companies affected |
|------|--------------------|
| `boards-api.greenhouse.io` | Celonis, N26, Trade Republic, HelloFresh, GetYourGuide, Contentful, Helsing, Black Forest Labs, Stability AI, Runway, Hightouch, Amplemarket, Isomorphic Labs, PhysicsX, Wayve, Scandit, Factorial, Boomi, Vercel, Airtable, Speechmatics, Ada, Glean, Hume AI, Arize AI, RunPod, Weights & Biases, Safari AI, Hootsuite, Later, Intercom, PolyAI, Temporal, Parloa, Anthropic |
| `api.ashbyhq.com` | Aleph Alpha, DeepL, ElevenLabs, n8n, Synthesia, Pinecone, Supabase, Lovable, Inngest, Resend, WorkOS, Clerk, Legora, Clay Labs, Glacis AI, Cradle, Photoroom, Faculty, Lakera, Attio, Travelperk, Klue, LangChain, Cohere, Vapi, Decagon, Zapier, Bland AI, Sierra, Deepgram, Lindy |
| `api.lever.co` | Mistral AI, Palantir, Spotify, Vinted, Qonto, Forto, Pigment, Clarity AI, Sanctuary AI |
| `api.smartrecruiters.com` | Siemens Energy, Syntegon |
| `apply.workable.com` | Hugging Face, Semios |

**56 additional companies** (HENSOLDT, Knorr-Bremse, Rohde & Schwarz, Infineon, MTU, Vector Informatik, Voith, Bertrandt, MAHLE, DEKRA, Dräger, and more) require a WebSearch handoff and were skipped.

**No jobs were added. No scan-history.tsv was updated.**

### Fix

Add these hosts to the network egress allowlist in your Claude Code on the web environment settings:

```
boards-api.greenhouse.io
api.ashbyhq.com
api.lever.co
api.smartrecruiters.com
api.workable.com
apply.workable.com
```

See: https://code.claude.com/docs/en/claude-code-on-the-web

Or run `/career-ops scan` in an interactive session (local Claude Code CLI) where these hosts are reachable.
