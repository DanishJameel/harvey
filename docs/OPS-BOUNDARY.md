# Opportunity Engine — ops boundary (Danish)

This checkout is the **client-hunting** runtime (Harvey). Keep these lines hard.

## Hard line — IZ Global

- Do **not** copy, paste, or re-implement Dialflow / Dialer / Aura **code, data, or architecture** from IZ Global into this repo.
- Public proof only: metrics and narrative already on https://danishjameel.me/work/dialflow (and private marketing drafts). No confidential internals.

## Lanes

| Lane | System | This repo? |
|------|--------|------------|
| Clients | Harvey (this fork) | Yes |
| Jobs | `ai-job-search` `/apply` etc. | No — separate |
| Investors (Aghaai) | Parked | No until unpark |

## Dual campaigns

- `voice` → train/proof https://danishjameel.me/work/dialflow  
- `outbound` → train/proof https://danishjameel.me/work/extractor  
- Never blend cohorts or Gate metrics.

## Send / domains

- Brand / human: `danishjameel.me` / `danish@danishjameel.me`  
- Cold From: **secondary domain** (deferred until after Phase 0–2 setup)  
- Aghaai admin email: **not** for client cold  

## Enrich

- Apollo / `enrich_providers` only as **offline batch → CSV → harvey import**  
- Never import job-search modules into the Harvey heartbeat  

See also: `ai-job-search/memory/design-opportunity-engine.md`
