# DIKWP-IMMUNET²

**Federated AI Risk Sensing, Semantic Quarantine, Revocation, Recovery and Mutual-Aid Commons**  
**联邦人工智能风险感知、语义隔离、能力撤销、恢复与互助公共免疫系统**

DIKWP-IMMUNET² is an offline-first reference implementation for the missing runtime between pre-deployment evaluation and ecosystem-wide AI incident response.

It does **not** begin with a fixed incident taxonomy. It derives a concept-erased relation kernel from identity, permission, tools, data boundaries, human control, externalities and DIKWP×DIKWP semantic transformations. Local nodes may share a minimal relation signature, but a federated alert cannot execute remote containment.

## Why it exists

Existing DIKWP repositories already provide semantic inquiry, purpose/permission control, agent traces, evidence ledgers, public authorization and cross-protocol cooperation. The missing public layer is a shared incident and recovery protocol that can:

- detect recurrent relation patterns across models and contexts;
- quarantine a narrow capability/context combination rather than ban an entire model;
- issue expiring, appealable local revocation tokens;
- prove rollback and limited recovery;
- share signatures without exporting raw sensitive data;
- preserve local authority and affected-party rights;
- turn false positives and failed recoveries into public test assets.

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e '.[dev]'
dikwp-immunet demo --base . --events 480 --seed 20260720
pytest -q
```

Without installation:

```bash
PYTHONPATH=src python -m dikwp_immunet2.cli demo --base .
```

Open `outputs/dashboard.html`.

## Main objects

- `IncidentCapsule`
- `FederatedAlert`
- `RevocationToken`
- `RecoveryProof`
- `AppealRecord`
- `MutualAidRequest`
- `Postmortem`

## Non-hierarchical response modes

`OBSERVE`, `VERIFY`, `SHADOW`, `ISOLATE_CONTEXT`, `REVOKE_CAPABILITY`, `FREEZE_RECOVER`, `ROLLBACK`, `RECOVER`, `SHARE_SIGNATURE`, `APPEAL`, `CLOSE`.

These are not maturity levels. They are scoped action modes selected by evidence, authority, reversibility, rights impact and service continuity.

## Safety boundary

See `docs/SYSTEM_BOUNDARY_CN.md`. All bundled events and nodes are synthetic. This project is not a compliance certification, a remote kill switch, or a production incident-response service.

## License

Apache-2.0.
