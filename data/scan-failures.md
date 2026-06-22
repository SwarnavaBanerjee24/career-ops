# Scan Failure Log

## 2026-06-19 — FAILED (network egress blocked)

**Result:** 0 of 85 companies reachable — all requests returned HTTP 403.

**Root cause:** The remote execution environment's network egress policy blocks outbound connections to job board APIs.

**Blocked hosts that need to be added to the egress allowlist:**

| Host | Example companies blocked |
|------|---------------------------|
| `boards-api.greenhouse.io` | Celonis, Helsing, Black Forest Labs, GetYourGuide, HelloFresh, N26, Trade Republic, SumUp |
| `api.ashbyhq.com` | n8n, Cohere, Zapier, ElevenLabs, DeepL, Aleph Alpha, Synthesia, Supabase, LangChain |
| `api.lever.co` | Mistral AI, Palantir, Qonto, Forto, Spotify, Vinted, Clarity AI |
| `api.smartrecruiters.com` | Siemens Energy, Syntegon |
| `apply.workable.com` | Hugging Face, Semios |

Additionally, 56 companies require WebSearch handoff which is also unavailable in this environment.

**Fix:** In your Claude Code on the Web session settings, add the 5 hosts above to the network egress allowlist. See https://code.claude.com/docs/en/claude-code-on-the-web for instructions.

**Impact:** No scan history was written, no new-jobs.md was updated. No data was lost — the next successful scan will pick up any jobs posted since the last successful run.

## 2026-06-21 — FAILED (network egress blocked)

**Result:** 0 of 85 companies reachable — all requests returned HTTP 403.

**Root cause:** Same as 2026-06-19. The remote execution environment's network egress policy blocks outbound connections to job board APIs. This issue has not been resolved since the first failure 2 days ago.

**Blocked hosts that need to be added to the egress allowlist:**

| Host | Example companies blocked |
|------|---------------------------|
| `boards-api.greenhouse.io` | Celonis, Helsing, Black Forest Labs, GetYourGuide, HelloFresh, N26, Trade Republic, SumUp |
| `api.ashbyhq.com` | n8n, Cohere, Zapier, ElevenLabs, DeepL, Aleph Alpha, Synthesia, Supabase, LangChain |
| `api.lever.co` | Mistral AI, Palantir, Qonto, Forto, Spotify, Vinted, Clarity AI |
| `api.smartrecruiters.com` | Siemens Energy, Syntegon |
| `apply.workable.com` | Hugging Face, Semios |

Additionally, 56 companies (HENSOLDT, Knorr-Bremse, Infineon, Rohde & Schwarz, MTU Aero Engines, Vector Informatik, Bertrandt, MAHLE, DEKRA, Dräger, Voith, etc.) require WebSearch handoff which is also unavailable in this environment.

**Fix:** In your Claude Code on the Web session settings, add the 5 hosts above to the network egress allowlist. See https://code.claude.com/docs/en/claude-code-on-the-web for instructions. Until this is fixed, no scans will succeed in this environment — run locally instead (`node scan.mjs`).

**Impact:** No scan history was written, no new-jobs.md was updated. No data was lost — the next successful scan will pick up any jobs posted since the last successful run.

## 2026-06-22 — FAILED (network egress blocked) — 3rd consecutive failure

**Result:** 0 of 85 companies reachable — all requests returned HTTP 403.

**Root cause:** Same persistent issue since 2026-06-19. The remote execution environment's network egress policy blocks outbound connections to job board APIs. **This has now failed 3 runs in a row (Jun 19, Jun 21, Jun 22) — no scan data has been collected in 3 days.**

**Blocked hosts that need to be added to the egress allowlist:**

| Host | Example companies blocked |
|------|---------------------------|
| `boards-api.greenhouse.io` | Celonis, Helsing, Black Forest Labs, GetYourGuide, HelloFresh, N26, Trade Republic, SumUp |
| `api.ashbyhq.com` | n8n, Cohere, Zapier, ElevenLabs, DeepL, Aleph Alpha, Synthesia, Supabase, LangChain |
| `api.lever.co` | Mistral AI, Palantir, Qonto, Forto, Spotify, Vinted, Clarity AI |
| `api.smartrecruiters.com` | Siemens Energy, Syntegon |
| `apply.workable.com` | Hugging Face, Semios |

Additionally, 56 companies (HENSOLDT, Knorr-Bremse, Infineon, Rohde & Schwarz, MTU Aero Engines, Vector Informatik, etc.) require WebSearch handoff which is also unavailable in this environment.

**Fix required (urgent):** In your Claude Code on the Web session settings, add the 5 hosts above to the network egress allowlist. See https://code.claude.com/docs/en/claude-code-on-the-web for instructions. Until this is fixed, no scans will succeed in this environment — run locally instead (`node scan.mjs`).

**Impact:** No scan history was written, no new-jobs.md was updated. No data was lost — the next successful scan will pick up any jobs posted since the last successful run.
