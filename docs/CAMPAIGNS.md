# Dual campaigns — voice + outbound

Train outputs (gitignored local configs):

| File | Campaign | Proof link |
|------|----------|------------|
| `harvey.local.voice.yaml` | `voice` | https://danishjameel.me/work/dialflow |
| `harvey.local.outbound.yaml` | `outbound` | https://danishjameel.me/work/extractor |
| `harvey.local.yaml` | **Active** (Harvey reads this) | whichever you copied last |

Skills snapshots:

- `skills/campaigns/voice/`
- `skills/campaigns/outbound/`

## Switch active campaign (PowerShell)

```powershell
cd c:\Users\Danish\src\ai-job-search\harvey

# Activate VOICE
Copy-Item -Force harvey.local.voice.yaml harvey.local.yaml
Copy-Item -Force skills\campaigns\voice\* skills\

# Activate OUTBOUND
Copy-Item -Force harvey.local.outbound.yaml harvey.local.yaml
Copy-Item -Force skills\campaigns\outbound\* skills\
```

Then `harvey status` / dashboard. Do **not** cold-send until secondary domain + warmup.

## Notes

- Site crawl trains the whole `danishjameel.me` graph (homepage + both cases), so both YAMLs overlap; use proof URL + offer framing per campaign when reviewing Outbox.
- `postal_address` is set to `Lahore, Punjab, Pakistan` — replace with a street / PO box / virtual mailbox when you have one (CAN-SPAM).
- Persona email is `danish@danishjameel.me` (human). Cold **From** still needs secondary mailbox later.
- `require_approval: true`, `max_daily_claude_percent: 55`, `max_daily_sends: 20` until warmup.
