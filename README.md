# CyberGuard AI — Analytics Platform for Cash Withdrawal Prediction in Phishing Cyber Crime

**Smart India Hackathon 2026** | Problem Statement ID: `26184` | Theme: Blockchain & Cybersecurity | Team: **Caraxes Crew**

> Reached Round 2 of SIH 2026. Sharing the idea and design here for reference and feedback.

## 🎯 Problem

When a victim loses money to a phishing/cybercrime scam, the stolen funds move rapidly through a chain of **mule accounts** before being withdrawn — usually before investigators can catch up. Manual tracing is too slow to stop the cash-out.

## 💡 Proposed Solution

1. Victim raises a cybercrime complaint with transaction details.
2. An ML model extracts key info from the complaint (transaction ID, amount, time, bank details).
3. A **Graph Neural Network (GNN)** traces the money flow across mule accounts, building the chain: **Victim → Mule Accounts → Final Suspected Account**.
4. The system retrieves the bank/branch of the final suspected account.
5. A predictive model estimates the **likely region and time window** where the cash may be withdrawn.
6. Account, branch, and region details are sent to the **nearest police station** via an authorized officer dashboard for human-verified action.

## 🧩 Key Innovations

- ML-based complaint analysis
- Automated mule-account tracing via GNNs
- Withdrawal region prediction (spatio-temporal modelling)
- Direct intelligence routing to the nearest police station

## 🏗️ Technical Approach

**Phase 1 – Data Acquisition:** Citizen complaint + bank/enforcement transaction data → Transaction database
**Phase 2 – Intelligence Processing:** Complaint analysis engine extracts key fields → builds a transaction/fraud network graph
**Phase 3 – Predictive Modelling & Alerting:** Outputs fraud risk score, possible cash-out area, confidence level, predicted time window
**Phase 4 – Human Verification & Action:** Alerts flow to an authorized officer dashboard for verification before any action is taken

### System Architecture
- **User Layer:** Citizen, Authorized Officer, Admin
- **Application Layer:** React (frontend) + FastAPI (backend)
- **AI & Analytics Layer:** Complaint analysis, risk scoring, location & time prediction
- **Data Layer:** Complaint DB, historical data, GIS data
- **Security & Governance Layer:** Authentication, role-based access, human verification, encryption

### Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite |
| Backend | FastAPI, Python 3, Uvicorn |
| AI / ML | NetworkX, Scikit-learn (GNN-based money-flow tracing) |
| Database | PostgreSQL, SQLAlchemy |
| GIS & Visualization | Leaflet / OpenStreetMap |

## 📈 Feasibility Highlights

- Vectorized spatial-decay calculations + PostGIS R-Tree queries for sub-100ms latency at scale
- Uses fields already logged by the existing 1930 cybercrime helpline — no change to police intake process needed
- Designed as decoupled microservices (FastAPI + PostGIS + React) to avoid single points of failure
- Acts as a **force-multiplier** for cyber cell teams rather than replacing human investigation

## 🌍 Impact

- Enables early identification of high-risk cybercrime cases
- Helps authorities act before further financial damage occurs
- Reduces time/cost of analyzing large complaint volumes
- Aligned with UN SDGs: Industry, Innovation & Infrastructure (9); Peace, Justice & Strong Institutions (16); Decent Work & Economic Growth (8); Sustainable Cities & Communities (11)

## 👥 Business Model Snapshot

- **Target users:** I4C nodal officers, state/district cyber cell heads, local field officers
- **Value:** Proactive fraud interception, precise actionable intelligence, resource optimization for law enforcement
- **Revenue model:** Government funding/grants (B2G), with potential future extension to private banks

## 📚 References

- [arXiv:2502.07111](https://arxiv.org/abs/2502.07111) — AI-powered prediction & tracking of cybercrime transactions
- [Springer, Spatial and Temporal Analysis for Cybercrime Risk Assessment (2024)](https://link.springer.com/article/10.1007/s11704-024-40474-v)
- [ASCE Library, Data-Driven Approaches for Resilient Infrastructure and Cybersecurity](https://ascelibrary.org/wiki/10.1061/9780784448265.132)
- NeurIPS 2025 — Predictive Cybercrime Intervention with Large Language Models and Graph Reasoning

## 🏆 Status

Built for Smart India Hackathon 2026 (Team Caraxes Crew). Advanced to Round 2 evaluation.

---
*This repository documents the idea, architecture, and design produced during SIH 2026. Contributions and feedback are welcome.*
