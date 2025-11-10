# Architecture Overview

## Today’s stack
- **e-spark-ccs** (backend): Firestore/Postgres (sessions, intensity), calculators (VM0038/RED), REST.
- **e-spark-app** (frontend): project onboarding + calc views.

## Integration plan (no rewrite)
1) **Guardian** (local or hosted):
   - Policy: `eSpark_VM0038_RED_v0.1`
   - Schemas: SessionMeasurement, IntensityHour, ComputationResult, Certificate
2) **CCS Adapter**:
   - POST `/guardian/submit/measurement` → upload sessions/intensity to Guardian
   - POST `/guardian/compute` (mode: "VM0038"|"RED_IE_NORA") → trigger policy action
   - GET  `/guardian/certificates/:vcId` → fetch VC
3) **App**:
   - Button: “Submit to Guardian”
   - Button: “Issue VC”
   - Card: VC hash + Hedera topic + HTS ref

## System diagram

```mermaid
flowchart LR
  CCS[CCS Backend] -->|Sessions & Intensity| Guardian[Hedera Guardian]
  
  App[Frontend App] -->|Trigger submit/compute| CCS
  
  Guardian -->|Issue VC JSON LD| CCS
  
  CCS -->|Anchor VC hash| HTS[Hedera Token Service]
  
  App -->|Show VC + HTS ref| CCS



