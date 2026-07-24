# 09 — Deadline Analysis

Honest time estimate vs deadline reality check.

---

## Timeline

| Milestone | Date |
|-----------|------|
| Today | July 24, 2026 |
| **Prototype Submission** | **July 26, 2026** |
| Time Remaining | **~2 days (48 hours)** |

## Total Work Estimate

| Phase | Hours | Parallelizable? |
|-------|-------|----------------|
| Phase 0: Fix Bugs | 2-3h | No |
| Phase 1: Design System | 2-3h | After P0 |
| Phase 2: Core UI | 5-7h | After P1 |
| Phase 3: Pages | 6-8h | After P2 |
| Phase 4: 3D + Particles | 3-4h | After P3 |
| Phase 5: Backend | 8-10h | **Parallel with P1-4** |
| Phase 6: Data Seeding | 4-6h | After P5 |
| Phase 7: Deploy + QA | 3-4h | After P4, P5, P6 |
| **Total Sequential** | **33-45h** | |
| **Total Parallel** | **~25-30h** | |

## If Working Solo

| Scenario | Hours/Day | Days Needed | Verdict |
|----------|-----------|-------------|---------|
| Realistic | 10h | 2.5-3 | ❌ Tight |
| Intense | 14h | 2 | ⚠️ Barely |
| All-nighter | 24h | 1.5 | ⚠️ Risky |

## If Working as Team (2 people)

| Scenario | Verdict |
|----------|---------|
| Split Frontend/Backend | ✅ Feasible in 2 days |

## MVP (Must Have)

- [ ] Frontend on Catalyst Slate
- [ ] 3+ pages working (Login, Overview, District Detail)
- [ ] Backend returning data from Catalyst Data Store
- [ ] Seed data in 5+ tables
- [ ] Working charts (recharts)
- [ ] SOC design theme
- [ ] Public GitHub repo + demo video

## Should Have

- [ ] All 4 pages
- [ ] 3D globe on login
- [ ] Particle backgrounds
- [ ] Page transitions

## Cut if Needed

- [ ] Postprocessing bloom
- [ ] Animated stat counters
- [ ] Sparkline charts
- [ ] Sortable district panel

## Critical Path

```
Phase 0 → 1 → 2 → 3 → 7 (deploy)
                    ↑
            Phase 5 → 6
```

**Bottleneck:** Backend (Phase 5) + Data Seeding (Phase 6) — must complete before deployment.

## Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| Catalyst CLI issues | Medium | High | Test early |
| ZCQL syntax | High | Medium | Start simple |
| Data seeding slow | High | Medium | Start with 5 tables |
| CORS misconfig | High | Medium | Test cross-origin early |

## Recommended Strategy

### Day 1 (July 24): Foundation + Core UI
- Morning: Phase 0 + Phase 1 (4h)
- Afternoon: Phase 2A + 2B (4h)
- Evening: Phase 3A (4h)

### Day 2 (July 25): Pages + Backend + Deploy
- Morning: Phase 3B + 3C (4h)
- Afternoon: Phase 4 + Phase 5 core (4h)
- Evening: Phase 6 + Phase 7 (4h)

### Day 3 (July 26): Polish + Submit
- Fix issues, record demo, write brief
- **Submit by deadline**

---

*Generated: 2026-07-24*