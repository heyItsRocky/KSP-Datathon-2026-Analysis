# 02 — Official Database Schema

The official 26-table schema from the ER diagram and Catalyst Data Store requirements.

---

## Core Case Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| CrimeMaster | Master crime record | crime_id, crime_no, crime_type, date_occurred, status |
| CrimeHead | Crime classification | head_id, head_name, head_code, category |
| Act | Legal acts/statutes | act_id, act_name, act_year, description |
| Section | Sections of acts | section_id, act_id, section_number |
| CrimeNo | Crime number assignment | crime_no_id, format, year, serial |
| FIR | First Information Report | fir_id, crime_id, complainant_id, officer_id |
| CaseMaster | Case tracking | case_id, crime_id, fir_id, case_status |
| ChargeSheet | Charges filed | sheet_id, case_id, accused_id, charges |

## Geography Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| State | State info | state_id, state_name, population |
| District | District info | district_id, district_name, state_id, area |
| PoliceUnit | Police stations | unit_id, unit_name, district_id, type |
| Court | Court hierarchy | court_id, court_name, court_type, district_id |

## Personnel Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| Employee | Police personnel | emp_id, name, rank_id, designation_id |
| Rank | Rank hierarchy | rank_id, rank_name, rank_level |
| Designation | Role designations | designation_id, designation_name |
| Department | Departments | dept_id, dept_name |

## Relationship Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| Victim | Victim records | victim_id, crime_id, name, age, gender |
| Accused | Accused persons | accused_id, crime_id, name, age |
| Complainant | Complainants | complainant_id, crime_id, name |
| Witness | Witnesses | witness_id, crime_id, name, statement |

## Cyber Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| CyberCrime | Cyber records | cyber_id, crime_id, attack_type, severity |
| CyberIncident | Incident tracking | incident_id, cyber_id, timestamp, status |
| ThreatActor | Threat actors | actor_id, alias, affiliation, risk_level |
| IOCTypes | Indicators of Compromise | ioc_id, type, value, confidence |

## Intelligence Tables
| Table | Purpose | Key Columns |
|-------|---------|-------------|
| IntelBrief | Intelligence briefs | brief_id, title, classification, content |
| IntelSource | Sources | source_id, source_name, reliability |
| IntelLink | Brief-source linking | link_id, brief_id, source_id |
| IntelReport | Filed reports | report_id, brief_id, report_type, status |

---

**Total: 26 tables** — All must be created in Catalyst Data Store.

*Generated: 2026-07-24*