# e-Spark-Ascension-Hackathon
reporitory for Ascension Hackathon

# e-Spark — Carbon Certification Solution (Ascension Hackathon)

**Goal:** Connect the existing e-Spark CCS + e-Spark APP to **Hedera Guardian** for digital MRV, and demonstrate issuance of voluntary carbon credits(VCs) for EV charging / REDIII (NORA IE) with **Hedera HTS** anchoring.

## What’s here (today)
- 📁 `docs/` — architecture overview, submission notes, progress log
- 📁 `status/` — current stack snapshot and milestones
- ⚙️ CI stub for typechecks/tests (to be wired when code lands)

## What exists already (separate repos)
- Backend: `e-spark-ccs` (data model: Projects, Sites, Chargers, Sessions, IntensityHours, CalcResults)
- Frontend: `e-spark-app` (project onboarding, calculations views)

> We’ll integrate Guardian **without** rewriting these repos: a thin adapter in CCS + a small UI action in the App.

## Hackathon scope
1. Guardian policy import (`Measurement → Computation → Certificate`)
2. CCS → Guardian adapter (3 endpoints)  
3. Issue VC for a date range & anchor on Hedera (HTS ref)
4. Publish artifacts and progress transparently in this repo

👉 See **docs/ASCENSION_SUBMISSION.md** for the judge-facing summary and demo flow.  
👉 See **docs/PROGRESS_LOG.md** for dated updates (we’ll append every session of work).

## Quick links
- Architecture: `docs/ARCHITECTURE_OVERVIEW.md`
- Progress log: `docs/PROGRESS_LOG.md`
- Current stack snapshot: `status/CURRENT_STACK.md`
- Milestones: `status/MILESTONES.md`
