# 10 — ULTRON GitHub Reference Analysis

Analysis of `ADITYA02NM/Datathon-2026-ULTRON` reference repository.

---

## Repository Overview

| Aspect | Detail |
|--------|--------|
| **Repo** | `https://github.com/ADITYA02NM/Datathon-2026-ULTRON` |
| **Files** | 258 |
| **Frontend** | React 19 + Vite + TypeScript + Tailwind |
| **Backend** | FastAPI (Python) |
| **Key Docs** | PRD.md, README.md, changes.md, split.md |

## PRD.md (128 lines)

**Product:** ULTRON — AI-driven crime analytics for SCRB.

**Target Architecture:**
| Component | Current | Target |
|-----------|---------|--------|
| Frontend | React + Vite | Catalyst Slate |
| Backend | FastAPI | Catalyst Functions |
| Database | PostgreSQL | Catalyst Data Store |
| ML | scikit-learn | Zia AutoML |

**5 ML Models:**
1. Risk Score Generator (Random Forest)
2. Anomaly Detection (Isolation Forest)
3. Phishing Detection (Logistic Regression)
4. Predictive Zones (ARIMA/Prophet)
5. MO Matcher (TF-IDF + Cosine)

## split.md (225 lines)

**Team:** Backend Person + Frontend Person

**8 Rules:**
1. Log changes in changes.md
2. One task at a time
3. Test before done
4. Document breaking changes
5. Seed data first
6. Catalyst deployment mandatory
7. Commit often
8. Never delete without asking

**15+ API Contracts** with exact response shapes.

## Frontend Packages

| Package | Our Equivalent |
|---------|---------------|
| zustand | ✅ (to install) |
| motion | ✅ (installed) |
| sonner | ✅ (to install) |
| clsx, tailwind-merge | ✅ (to install) |
| lucide-react | ✅ (installed) |
| recharts | ✅ (installed) |
| leaflet | ✅ (installed) |
| cytoscape | ❌ Not needed |
| @xyflow/react | ❌ Not needed |
| three/cobe/particles | ❌ Not in ULTRON |

## What We Can Learn

### Adopt
1. Feature-based architecture
2. Zustand stores
3. Sonner toasts
4. API contract definition

### We Have They Don't
1. Three.js + R3F (3D)
2. Cobe (globe)
3. TSParticles (effects)
4. Postprocessing (bloom)

---

*Generated: 2026-07-24*