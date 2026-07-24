# 11 — Current Codebase Analysis

Actual state of the astra/ codebase at `/home/Rakshith/opencode/astra/`.

---

## Pages (4)

| Page | File | Status |
|------|------|--------|
| Overview | `pages/Overview.tsx` | ⚠️ Uses JSON, not API |
| CyberCrime | `pages/CyberCrime.tsx` | ⚠️ Uses JSON, not API |
| District Detail | `pages/DistrictDetail.tsx` | ❌ Stub (shows "--") |
| Not Found | `pages/NotFound.tsx` | ✅ Works |

## Components (8)

| Component | Status |
|-----------|--------|
| AppLayout | ✅ Fixed sidebar + header |
| Sidebar | ✅ 3 nav items, collapsible |
| Header | ✅ Title + search + bell |
| Badge | ✅ Color variants |
| Card | ✅ Basic wrapper |
| StatCard | ✅ Icon + label + value + trend |
| LoadingSpinner | ✅ Loading state |
| KarnatakaChoroplethMap | ✅ Leaflet choropleth |

## Hooks (2)

| Hook | Status |
|------|--------|
| useCrimeData | ✅ React Query hook |
| useDistrictData | ✅ Exists, unused by DistrictDetail |

## API Client (4 functions)

- `fetchOverviewData()` → GET /api/overview
- `fetchDistricts()` → GET /api/districts
- `fetchDistrictDetail()` → GET /api/district/:code
- `fetchCyberData()` → GET /api/cyber

**Bug:** Pages import `district-stats.json` directly instead of using these.

## Backend (4 endpoints)

- GET /api/overview
- GET /api/districts
- GET /api/district/{code}
- GET /api/cyber

Database: SQLite with 2 models (CrimeRecord, DistrictMeta).

## Installed 3D/Effects (unused)

- three, @react-three/fiber, @react-three/drei
- @react-three/postprocessing
- @tsparticles/react, tsparticles-slim
- cobe
- motion

## CSS Highlights

- `.glass-card` — backdrop blur + border
- Custom scrollbar styles
- Leaflet dark theme overrides
- fadeIn + countUp keyframe animations

## What's Missing

| Gap | Impact |
|-----|--------|
| Login page | Can't demo auth flow |
| SOC theme (HUD, glow, scanlines) | Doesn't look like command center |
| Page transitions | No animation between routes |
| Catalyst deployment | Can't submit |
| 26-table schema | Only 2 models |
| Seed data | Only 27 districts |
| Animated counters | No number animation |
| 3D globe integration | Installed but unused |
| Particle backgrounds | Installed but unused |

---

*Generated: 2026-07-24*