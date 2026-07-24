# 05 — Backend Architecture

Catalyst Functions architecture for the crime analytics backend.

---

## Endpoint Design

| Function | Method | Path | Purpose |
|----------|--------|------|---------|
| getOverview | GET | `/api/overview` | Dashboard aggregate stats |
| getDistricts | GET | `/api/districts` | All 31 districts |
| getDistrictDetail | GET | `/api/district/:code` | Single district |
| getCrimeList | GET | `/api/crimes` | Crime records with filters |
| getCrimeDetail | GET | `/api/crime/:id` | Single crime record |
| getCyber | GET | `/api/cyber` | Cyber crime stats |
| getCyberList | GET | `/api/cyber/list` | Cyber incidents |
| getHotspots | GET | `/api/hotspots` | Crime hotspot data |
| getAnomalies | GET | `/api/anomalies` | Anomaly detection |
| getIntelBriefs | GET | `/api/intel/briefs` | Intelligence briefs |
| getIntelSources | GET | `/api/intel/sources` | Intelligence sources |
| getPredictions | GET | `/api/predictions` | Predictive analytics |
| searchCrime | GET | `/api/search` | Full-text search |
| getTrends | GET | `/api/trends` | Time-series trends |
| getComparison | GET | `/api/compare` | District comparison |

## Data Flow

```
Frontend (React)
    ↓ fetch()
API Gateway (CORS, Auth)
    ↓ route
Catalyst Functions (Python)
    ↓ ZCQL query
Catalyst Data Store (26 tables)
    ↓ result
Response JSON → Frontend → Recharts
```

## Function Structure

```
functions/
├── getOverview/index.py
├── getDistricts/index.py
├── getDistrictDetail/index.py
├── getCrimeList/index.py
├── getCyber/index.py
└── shared/
    ├── db.py          (ZCQL connection)
    ├── queries.py     (reusable queries)
    └── auth.py        (Catalyst auth)
```

## Example Function

```python
import json
from catalyst import CatalystApp, DataStore

def handler(context):
    app = CatalystApp(context)
    ds = DataStore(app)
    
    total_crimes = ds.zcql_query("SELECT COUNT(*) FROM CrimeMaster")
    districts = ds.zcql_query("SELECT district_name FROM District")
    cyber_count = ds.zcql_query("SELECT COUNT(*) FROM CyberCrime")
    
    return {
        "statusCode": 200,
        "body": json.dumps({
            "totalCrimes": total_crimes,
            "totalDistricts": len(districts),
            "cyberCrimes": cyber_count,
            "status": "active"
        })
    }
```

---

*Generated: 2026-07-24*