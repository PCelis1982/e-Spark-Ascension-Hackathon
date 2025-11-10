# Ascension Hackathon Submission (e-Spark)

## One-liner
Digital MRV for EV charging aligned with VM0038/REDIII via Hedera Guardian + HTS.

## Problem
Charging infra is high CAPEX/OPEX; MRV automates credit value and makes small assets viable when aggregated.

## What we’re submitting
- Guardian policy + CCS adapter to issue a **Certificate VC** from real session data (date-range).
- HTS anchoring reference of the VC hash (immutable audit pointer).
- Transparent progress logging and artifacts in this repo.

## Demo flow
1. Upload measurement → CCS posts to Guardian
2. Compute in policy (select VM0038 or RED_IE_NORA)
3. Guardian issues VC → we display hash/topic; (optional) mint HTS ref
4. Judges can inspect artifacts here in `docs/` and the Progress Log

## Team & roles
- [Pablo Celis](https://ie.linkedin.com/in/pablojeremias) - Product Lead
- [Emiliano Celis](https://www.linkedin.com/in/celisemiliano/) - Technical Lead
- [Patrick Flynn](https://www.linkedin.com/in/patrick-flynn-1ba9191b0/) - Sustainability Lead
