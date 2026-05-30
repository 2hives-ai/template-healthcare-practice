# Healthcare practice

A starter Hive for a GP clinic, specialist practice, allied-health practice, or dental clinic. Six lanes covering intake, scheduling, clinical records, billing, privacy, ops.

**This template is for OPERATIONAL records. Clinical records remain in your clinical system (Best Practice / Medical Director / equivalent). NEVER put identified patient health information in this repo.**

## What's in this template

| Directory | What lives here | Agent role |
|---|---|---|
| `patient-intake/` | New patient registration workflow, forms, ID verification | Intake coordinator |
| `scheduling/` | Appointment book ops, recall calendar, cancellations | Scheduling |
| `clinical-records/` | Operational metadata + pointers to clinical system. NO PHI bodies. | Records officer |
| `billing-claims/` | Medicare / DVA / private health claims, gap fees, accounts | Billing |
| `privacy-compliance/` | Privacy Act compliance, breach response, health-record retention | Privacy officer |
| `practice-operations/` | Roster, supplies, equipment, accreditation, HR | Practice manager |

## Tier-based provisioning

- **Tier 1:** all 6 auto-start.
- **Basic:** `scheduling/` + `billing-claims/` is the typical pair for a small practice.

## Jurisdictional notes

- Defaults to AU (Medicare, DVA, AHPRA registrations, state health record retention rules — varies).
- **AHPRA registrations** + CPD per practitioner — in `practice-operations/`.
- **Privacy Act + APPs + My Health Records Act** apply — `privacy-compliance/`.

## CRITICAL — what this template is NOT

- **Not a clinical system.** Clinical notes, diagnoses, prescriptions, results — all live in your clinical software, never here.
- **Not a substitute for clinical judgment.** No agent gives clinical advice.
- **Not where you store PHI bodies.** Use patient IDs (your practice's internal patient number) for any reference; the ID → identified data mapping stays in your clinical system.

## Suggested first steps

1. `scheduling/` — current week's appointment book at the operational level.
2. `billing-claims/` — claims pipeline + Medicare item-number quick reference.
3. `patient-intake/` — new-patient workflow you already use.
4. `practice-operations/` — roster + accreditation cycle.
5. `privacy-compliance/` — Privacy Act register + breach response plan.
6. `clinical-records/` — operational metadata only (e.g. recall lists by ID, not by name).

## Customising

Add: `nursing-clinic/`, `vaccination-clinic/`, `chronic-disease/`, `mental-health/`, `referrals/`, `pathology/`.
