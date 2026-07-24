# 08 — Execution Plan

Phase-by-phase build order with dependencies, time estimates, and deliverables.

---

## Build Order

```
Phase 0: Fix Bugs & Data Foundation
    ↓
Phase 1: Design System
    ↓
Phase 2: Core UI (Login + Layout)
    ↓
Phase 3: Pages (Overview + CyberCrime + District Detail)
    ↓
Phase 4: 3D + Particles + Motion
    ↓
Phase 5: Backend Migration (Catalyst)
    ↓
Phase 6: Data Seeding (26 Tables)
    ↓
Phase 7: Deployment + QA
```

## Phase 0: Fix Bugs & Data Foundation (2-3h)

| Task | Time | Priority |
|------|------|----------|
| Install zustand, sonner, clsx, tailwind-merge | 10min | High |
| Fix district mismatch (27→31) | 1h | High |
| Wire DistrictDetail to useDistrictData hook | 30min | High |
| Fix data source bugs (JSON→API) | 1h | High |

## Phase 1: Design System (2-3h)

| Task | Time | Priority |
|------|------|----------|
| CSS custom properties (navy/cyan palette) | 30min | High |
| Glassmorphism classes (.glass-card glow) | 30min | High |
| HUD corner notch CSS (.hud-frame) | 20min | High |
| Status pulse animation | 15min | Medium |
| Google Fonts (Inter + JetBrains Mono) | 5min | High |
| Tailwind @theme tokens | 30min | High |

## Phase 2: Core UI (5-7h)

### 2A: Login Page (3-4h)
| Task | Time | Priority |
|------|------|----------|
| CobeGlobe component | 1h | High |
| ParticlesBackground | 1h | High |
| GlassmorphismLogin card | 1h | High |
| AnimatePresence transitions | 30min | High |

### 2B: Layout Shell (2-3h)
| Task | Time | Priority |
|------|------|----------|
| SOCSidebar (ASTRA branding) | 1h | High |
| SOCHeader (clock, LIVE indicator) | 1h | High |
| PageTransition wrapper | 30min | Medium |

## Phase 3: Pages (6-8h)

| Task | Time | Priority |
|------|------|----------|
| Animated stat counters | 1h | High |
| DistrictBarChart (recharts) | 1h | High |
| MonthlyTrendChart (area) | 1h | High |
| CrimeCategoryPie (donut) | 30min | Medium |
| Threat level banner | 30min | High |
| IncidentTypeChart | 1h | High |
| CyberTrendLine | 1h | High |
| District Detail fix + 4 charts | 1.5h | High |

## Phase 4: 3D + Particles + Motion (3-4h)

| Task | Time | Priority |
|------|------|----------|
| CobeGlobe on Overview (widget) | 1h | Medium |
| Postprocessing bloom | 1h | Medium |
| Scroll animations | 1h | Low |
| Hover effects | 30min | Low |
| Particle background | 30min | Medium |

## Phase 5: Backend Migration (8-10h)

| Task | Time | Priority |
|------|------|----------|
| Catalyst project setup | 1h | High |
| 26 Data Store tables | 2h | High |
| 5 core Functions | 4h | High |
| 10 additional endpoints | 4h | Medium |
| API Gateway config | 1h | High |

## Phase 6: Data Seeding (4-6h)

| Task | Time | Priority |
|------|------|----------|
| Seed lookup tables | 1h | High |
| Seed geography | 1h | High |
| Seed personnel | 1h | High |
| Seed cases (500+ FIRs) | 2h | High |
| Seed relationships | 1h | High |
| Verify FK integrity | 30min | High |

## Phase 7: Deployment + QA (3-4h)

| Task | Time | Priority |
|------|------|----------|
| Deploy frontend to Slate | 30min | High |
| Deploy functions | 30min | High |
| Verify all endpoints | 1h | High |
| Fix deployment issues | 1h | High |
| Record demo video | 1h | High |
| Write prototype brief | 1h | High |

## Parallel Tracks

```
Track A (Frontend): Phase 0 → 1 → 2 → 3 → 4 → 7
Track B (Backend):  Phase 5 → 6 → 7
```

---

*Generated: 2026-07-24*