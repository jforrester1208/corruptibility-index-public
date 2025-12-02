# CI_DESIGN_DOCUMENT_PUBLIC_V1.0.md
**Version:** 1.0 (Internal Protected)  
**Author:** John Forrester  
**Status:** Locked for IP Protection  
**Last Updated:** December 2025

---

# 1. Introduction

## 1.1 Purpose of This Document
This document defines the complete internal design architecture, metric system, subsystem framework, data-source model, scoring logic, and algorithmic strategies of the **Corruptibility Index (CI)** platform.  
It is intended as an **internal-protected, IP-establishing artifact**, documenting the full conceptual and structural invention created by **John Forrester**.

This file is written in pure Markdown (`.md`) and is suitable for:
- inclusion in private Git repositories,
- submission as evidence of prior invention,
- supporting trademark filings for CI product lines,
- internal engineering onboarding,
- internal legal/strategy review.

## 1.2 Scope
This Version 1.0 design document includes:
- Finalized **CI-Core** metric set (11 metrics)
- Canonical **CI Subsystem Architecture** (CI-Background, CI-Watch, CI-Screen, CI-Monitor)
- Complete **Metric → Data Source → API** mapping
- Internal-only **metric computation notes**
- Normalization, scoring, and risk-model logic
- Ethics, security, and misuse-prevention
- Implementation notes, pseudocode patterns, and roadmap

## 1.3 Intellectual Property Framing
This document is structured to demonstrate:
- **Originality** of conceptual framework
- **Novelty** of subsystem architecture
- **Non-obviousness** of metric interrelation
- **Structured technical expression** suitable for copyright and invention record

This is not a public-facing or marketing-facing document.  
It contains internal, protected details of the system.

---

# 2. System Overview

## 2.1 High-Level Description
The **Corruptibility Index (CI)** is a structured analytical scoring system that assesses the *corruption-risk profile* of public figures, political actors, appointees, and related entities.

The system ingests heterogeneous data sources—financial records, political disclosures, network associations, real estate acquisitions, legal events, and media signals—and converts them into **risk metrics**, which are normalized, weighted, and aggregated into a single composite score.

## 2.2 Design Principles
1. **Modularity:** Metrics operate as independent, testable risk signals.
2. **Explainability:** Each metric has clear diagnostic meaning.
3. **Traceability:** All data sources tied to public registries or documented APIs.
4. **Subsystem Extensibility:** Core scoring is just one product; the same architecture supports background checks, screening, monitoring, and long-term pattern tracking.
5. **Non-Predictive:** CI measures *risk exposure*, not deterministic outcomes.
6. **Defensibility:** Every metric yields interpretable, non-subjective inputs.

## 2.3 Architecture Summary
At the top level, CI consists of:

### **1. CI-Core**
The 11 primary corruption-risk metrics (flagship score).

### **2. CI Subsystems**
- **CI-Background:** static due-diligence and identity integrity
- **CI-Watch:** dynamic continuous monitoring
- **CI-Screen:** lightweight rapid filter
- **CI-Monitor:** long-term drift and trend analysis

### **3. Data Ingestion Layer**
- Public APIs
- Disclosures and registries
- Network graph computation
- Media and sentiment signals
- Legal filings and enforcement records

### **4. Transformation Layer**
Cleansing → normalization → metric-specific preprocessing.

### **5. Metric Scoring Engine**
Each metric produces a raw score, intermediate normalized score, and unitless risk signal.

### **6. Aggregation Layer**
Applies weights and interdependency rules, producing:
- CI-Core Score
- Subsystem-specific profiles

### **7. Audit Trail & Metadata**
Every signal is timestamped, sourced, and version-tracked.

---

# 2A. CI Subsystem Architecture (Locked Down)

The CI platform consists of five subsystems, each with its own metric family, purpose, and output format. Documenting these subsystems here establishes them as **original, integral components** of the invention.

## **CI-Core**
The flagship corruption-risk scoring engine.  
Uses 11 finalized metrics (see Section 3).

## **CI-Background**
Static due-diligence report generating:
- Identity integrity
- Litigation footprint
- Historical financial transparency
- Conflict-of-interest exposure
- Reputation deviation

Used for onboarding, vetting, research, and investigative prep.

## **CI-Watch**
Continuous monitoring system providing:
- Daily/weekly alerts
- Media and sentiment acceleration signals
- Real-time wealth-change anomalies
- Sudden legal exposure
- Network rewiring events

Functions as the “Bloomberg Terminal” layer of CI.

## **CI-Screen**
Lightweight rapid filter for:
- Hiring
- Appointments
- Volunteer/committee vetting
- Board candidacy checks

Low-cost, high-volume use case.

## **CI-Monitor**
Long-term trend and drift analytics:
- Multi-year wealth drift
- Policy consistency curves
- Donor/influence convergence
- Real-estate accretion
- Multi-cycle reputation gravitation

Ideal for editorial, academic, or institutional tracking.

**All subsystems derive from the same architectural foundation but employ unique metric sets.**  
This supports strong IP defensibility.

---

# 3. Metric Architecture — CI-Core (Finalized 11 Metrics)

This section documents the **official**, locked-in CI-Core metric set.  
Each entry includes description + internal computation notes (not full formulas).

---

## **3.1 Donor Metrics**
Measures concentration, clustering, and anomaly patterns in donor behavior.

### Inputs
- Donation registries
- PAC data
- Recurrence patterns
- Geographic clusters

### Internal Notes
- Use HHI-style concentration metrics
- Detect donor “families” and shells
- Compare donor diversity vs. expected baseline

---

## **3.2 Wealth Anomaly**
Detects misalignment between observed assets and plausible legitimate income.

### Inputs
- Property records
- Corporate affiliations
- Public financial disclosures

### Internal Notes
- Identify outlier purchases vs. declared income
- Normalize against regional and peer benchmarks
- Flag opaque beneficial ownership

---

## **3.3 Real Estate Patterning**
Flags real estate behaviors associated with risk:
- rapid flipping
- multi-property clusters
- shell-company transactions

### Inputs
- County/property registries
- Beneficial-owner mapping

### Internal Notes
- Track transaction velocity
- Identify interconnected holding structures

---

## **3.4 Lobbyist Entanglement**
Measures intensity and nature of interactions with lobbyists.

### Inputs
- Lobby registration datasets
- Meeting logs
- Disclosure forms

### Internal Notes
- Weighted for recency
- Penalizes undisclosed interactions

---

## **3.5 Transactional Appointments**
Detects appointments that coincide with:
- donations
- political favors
- network obligations

### Internal Notes
- Graph-based relationship modeling
- Identify “transactional clusters”

---

## **3.6 Policy Misalignment Risk**
Quantifies divergence between:
- public positions
- voting/actions
- donor/lobby alignment

### Internal Notes
- Compare stated vs. observed
- Detect ideological reversals timed with donations

---

## **3.7 Social Ecosystem Alignment Score**
Measures alignment between a subject and known high-risk actors.

### Inputs
- Social/media graph connections
- Re-posting behavior
- Endorsements

### Internal Notes
- Graph centrality + risk-weighted adjacency

---

## **3.8 Personal Conduct Anomalies**
Identifies personal behavior that correlates with future corruption exposure.

### Inputs
- Public records
- Ethics disclosures
- Repeated minor violations

### Internal Notes
- Treat as weak signals unless recurring

---

## **3.9 Legal Irregularities**
Flags legal activity indicative of elevated corruption risk.

### Inputs
- Civil suits
- Enforcement actions
- Regulatory penalties
- Investigations

### Internal Notes
- Time-weighted decay but never fully zero

---

## **3.10 Casino License Heuristic**
Pattern-recognition heuristic for:
- gambling exposure
- license holdings
- casino-related financial behaviors

### Internal Notes
- Very effective for identifying hidden financial risk vectors

---

## **3.11 Investigative Pressure Index**
Measures “heat” from:
- journalists
- watchdog groups
- investigators
- whistleblower signals

### Internal Notes
- Sentiment acceleration
- Clustering of simultaneous inquiries

---

# 4. Subsystem Metric Frameworks (Internal)

This section defines the **metric families used by the four CI subsystems** outside of CI-Core.  
These subsystems dramatically strengthen the CI project as a platform and significantly broaden the IP footprint.

Each subsystem is designed to:
- use different data sources from CI-Core,
- serve a different commercial use-case,
- and produce a distinct output format.

---

# 4.1 CI-Background (Static Due-Diligence)

## Purpose
Provide a **comprehensive static background report** on a subject, suitable for:
- research
- onboarding
- vetting
- pre-investigative preparation

## CI-Background Metric Categories
1. **Identity Integrity**
    - alias history
    - name continuity
    - shell company overlaps
    - identity anomalies

2. **Employment & Appointment Legitimacy**
    - rapid role changes
    - suspicious promotions
    - board-stacking patterns

3. **Litigation Footprint**
    - civil suits
    - regulatory cases
    - beneficial-owner disputes

4. **Financial Transparency Score**
    - declared vs. observed assets
    - opacity of entities
    - unexplained wealth gaps

5. **Conflict-of-Interest Baseline**
    - family-owned businesses
    - advisory roles
    - overlapping corporate directorships

6. **Known Risk Associations**
    - ties to high-risk individuals
    - links to sanctioned persons

7. **Historical Reputation Deviation**
    - long-term media tone patterns
    - unresolved controversies

---

# 4.2 CI-Watch (Continuous Monitoring)

## Purpose
Provide **real-time or periodic alerts** about emerging corruption-risk signals.

## CI-Watch Metric Categories
1. **Event-Driven Wealth Change Alerts**
    - sudden asset acquisitions
    - large debt extinguishments

2. **New Entity Formation Activity**
    - LLCs
    - nonprofits
    - trust structures

3. **Lobbying Signals (Real-Time)**
    - meeting logs
    - new engagements

4. **Policy-Shift Divergence Alerts**
    - abrupt reversals
    - deviation from baseline ideology

5. **Sudden Legal Exposure**
    - new investigations
    - new regulatory actions

6. **Network Rewiring**
    - new partnerships
    - new board overlaps
    - emergent clusters

7. **Media Velocity Breakouts**
    - spikes in mentions
    - concentrated negative tone

8. **Travel / Scheduling Anomalies**
    - repeated closed-door meetings
    - high-risk travel patterns

9. **Donor Cluster Movements (Short-Term)**
    - synchronized donor activity

10. **Investigative Noise Index (Daily)**
- journalist activity spikes
- watchdog clustering

---

# 4.3 CI-Screen (Lightweight Rapid Filter)

## Purpose
A **low-cost, fast-turnaround vetting tool** for employment, campaign staffing, board appointments, and volunteer positions.

## CI-Screen Metric Categories
1. **Recent Litigation Flags (Last 5 Years)**
2. **Disclosure Discrepancies**
3. **High-Risk Network Links**
4. **Prior Conflict-of-Interest Incidents**
5. **Career Gap Anomalies**
6. **Sanctions & Watchlist Checks**

**Designed for red/yellow/green output only.**

---

# 4.4 CI-Monitor (Long-Term Pattern Tracking)

## Purpose
Detect **slow-moving corruption trends** over years or decades.

## CI-Monitor Metric Categories
1. **Long-Arc Wealth Drift**
    - multi-year asset expansion
    - unexplained growth curves

2. **Policy Consistency Curves**
    - ideological stability vs. donor pressure

3. **Donor & Influence Convergence Over Time**
    - concentration of donors and backers

4. **Network Centrality Shifts**
    - rising or declining influence

5. **Legal Heatmap (Long-Term)**
    - persistent legal “background radiation”

6. **Real Estate Accretion Trends**
    - slow aggregation of properties

7. **Reputation Gravitation Index**
    - long-cycle sentiment movement

8. **Compliance Drift Score**
    - pattern of increasingly risky behavior

---

# 5. Data Source & API Map

This section provides the canonical **Metric → Data Source → API** table.  
This is important for IP protection because it documents the *specific structural mapping* of the CI system.

The table below includes CI-Core metrics and subsystem categories.

---

## 5.1 Metric → Data Source → API Table

| Metric / Category | Data Source | API / Access Method | Notes |
|------------------|-------------|----------------------|-------|
| Donor Metrics | FEC Filings, State Registries | FEC API, OpenSecrets API | Includes donor clustering and HHI analysis |
| Wealth Anomaly | Property Records, Financial Disclosures | County APIs, Public Asset Registries | Compare observed vs. declared assets |
| Real Estate Patterning | Deeds, Transfers, LLC Registries | County Clerk APIs | Detect shell transfers, rapid flipping |
| Lobbyist Entanglement | Lobby Disclosures | Senate Lobbying Disclosure API | Interaction intensity, recency |
| Transactional Appointments | Appointments, Boards, PAC Data | GovTrack API, OpenGov | Graph-based detection |
| Policy Misalignment Risk | Voting Records, Policy Statements | GovTrack, ProPublica Congress API | Detect reversals aligned with donations |
| Social Ecosystem Alignment | Social Graph, Media Links | Twitter/X API, YouTube API | Risk-weighted centrality |
| Personal Conduct Anomalies | Public Records | Court Record APIs | Weak signals unless repeated |
| Legal Irregularities | Civil/Criminal Filings | CourtListener API | Regulatory investigations |
| Casino License Heuristic | Gaming Licenses | State Gaming Regulatory APIs | Risk-indicator heuristic |
| Investigative Pressure Index | Watchdog Activity, Journalists | GDELT API, MediaCloud | Sentiment velocity and clustering |
| Identity Integrity (Background) | Corporate Registries | OpenCorporates API | Alias continuity |
| Litigation Footprint (Background) | Court Records | CourtListener | Cases & violations |
| Financial Transparency (Background) | Disclosures | State Ethics APIs | Compare declared vs. observed |
| Event-Driven Alerts (Watch) | Property, Donor, Lobby Data | FEC, County APIs | For CI-Watch alerts |
| Network Rewiring (Watch) | Directorships, Boards | LittleSis API | Graph changes |
| Reputation Drift (Monitor) | Media Archives | GDELT, MediaCloud | Multi-year sentiment |

---

# 6. Normalization Strategy (Internal Only)

Normalization is essential to prevent noise, ensure comparability, and create a **unitless, dimensionless risk signal** for every metric.

This is a **high-level strategy** sufficient for IP defensibility.

---

## 6.1 Cross-Metric Normalization
All raw metric values are transformed into **0–100 normalized risk scores** using:
- modified z-scores,
- log compression for heavy-tailed distributions,
- percent-rank normalization for categorical inputs.

---

## 6.2 Temporal Normalization
Event-driven metrics decay over time:
- exponential decay
- recency weighting
- different decay constants for each metric family

Example: legal events decay slower than media events.

---

## 6.3 Weight Class Hierarchy
Metrics fall into three weight classes:
- **High-Impact Metrics (30–40%)**
- **Mid-Impact Metrics (10–20%)**
- **Low-Impact Metrics (5–10%)**

CI-Core uses a mixed-class weight structure.

---

## 6.4 Noise Filtering
To prevent signal distortion:
- require repeated observations for weak signals
- ignore single anomalous data points
- apply cluster confirmation on network-related metrics

---

## 6.5 Distortion Risk Guardrails
Guardrails include:
- baseline vs. delta comparison
- avoid double-counting overlapping signals
- enforce metric independence where possible
- detect tautologies (e.g., donor networks + donor concentration)

Documenting these guardrails provides IP protection against misuse or misinterpretation.

---

# 7. Scoring Engine Architecture

This section defines the internal pipeline used to ingest data, compute metric signals, normalize them, and produce subsystem scores and the CI-Core composite.

It is intentionally detailed enough to support IP defensibility while not exposing proprietary formulas verbatim.

---

## 7.1 Overview of Scoring Pipeline
The engine consists of six stages:

1. **Data Ingestion Layer**
2. **Preprocessing & Transformation**
3. **Metric Computation**
4. **Normalization & Weighting**
5. **Aggregation to Subsystem Outputs**
6. **CI-Core Final Score Assembly**

Each stage is independent, testable, and version-controlled.

---

## 7.2 Stage 1 — Data Ingestion Layer

### Input Types
- Numeric data (donation amounts, asset values)
- Categorical data (sanction status, license status)
- Graph-based inputs (network relationships)
- Textual inputs (media references, sentiment signals)
- Time-series data (policy changes, donation flows)

### Ingestion Methods
- Pull-based APIs
- Push webhooks (where available)
- Batch scraping of public registries
- Scheduled data refresh (daily/weekly/monthly)

### Metadata
All ingested data includes:
- timestamp
- source
- source URL
- hash for integrity verification

---

## 7.3 Stage 2 — Preprocessing & Transformation

### Cleaning
- remove duplicates
- normalize names/entities
- address alias resolution
- standardize numeric precision

### Entity Linking
Link the subject to:
- directorships
- donors
- real estate properties
- legal cases
- lobbying interactions

### Graph Construction
A subject-specific graph is built for:
- donor clusters
- lobbyist networks
- board overlaps
- social/media ecosystems

Graph centrality measures (degree, betweenness, eigenvector) are computed here (not in the metric stage).

---

## 7.4 Stage 3 — Metric Computation

Each metric receives:
- cleaned inputs
- resolved entities
- optional graph-preprocessed values

Metrics then compute **raw scores** using internal logic such as:
- clustering coefficients
- delta patterns over time
- HHI concentration
- recency scaling
- adjacency-based risk scoring

Raw scores remain **unbounded** until normalization.

---

## 7.5 Stage 4 — Normalization & Weighting

Every metric is transformed to a 0–100 range via:
- z-score normalization
- log compression
- percentile ranking
- min/max bounding
- decayed historical weighting

The metric’s **weight class** is then applied.

---

## 7.6 Stage 5 — Subsystem Output Profiles

Each subsystem produces a distinct profile:

### **CI-Background Output**
- static report
- identity, litigation, transparency, conflict-of-interest

### **CI-Watch Output**
- rolling alerts
- dashboards
- time-series anomaly feeds

### **CI-Screen Output**
- binary or ternary flags (red/yellow/green)

### **CI-Monitor Output**
- long-term drift graphs
- slow-wave indicators

All subsystems are generated **before** CI-Core to ensure independence.

---

## 7.7 Stage 6 — CI-Core Final Score Assembly

### Weighted Aggregation Model
The final CI-Core score:
- aggregates normalized metric scores
- applies metric-specific weights
- applies subsystem-independent adjustments

### Risk Bands
The final numerical score is placed into risk bands:
- **0–19:** Very Low
- **20–39:** Low
- **40–59:** Moderate
- **60–79:** High
- **80–100:** Severe

Risk bands are used for interpretation, not scoring.

---

# 8. Security, Ethics, and Abuse Prevention

Because CI deals with public-figure analytics, certain ethical and operational guardrails are mandatory.

This section also strengthens IP claims by defining the responsible-use framework.

---

## 8.1 Security Principles

### Authentication & Authorization
- API keys
- user access tiers
- audit logs

### Data Protection
- hashing of data sources
- encrypted storage of sensitive metadata
- verified provenance

### Anti-Tampering
- version-locking each metric
- reproducible scoring environment

---

## 8.2 Ethics & Fairness Guidelines

1. **Transparency:**  
   A user must be able to understand why a score went up or down.

2. **No Predictive Claims:**  
   CI measures **risk exposure**, not criminal likelihood.

3. **Anti-Bias Controls:**
    - no demographic variables
    - no protected-class inputs
    - no sentiment weighting based on identity categories

4. **Source Integrity:**  
   Only public, legally accessible sources are used.

5. **Proportionate Interpretation:**  
   Weak signals are never interpreted as strong findings unless repeated.

---

## 8.3 Anti-Gaming Measures

- detect anomalous data removal
- detect sudden donation “whitewashing”
- identify graph-disrupting attempts
- compare historical vs. current entity structures

These measures help maintain systemic integrity.

---

## 8.4 Misuse Prevention

CI should not be used for:
- personal vendettas
- non-public individuals
- harassment
- disinformation campaigns

Any enterprise-facing product includes clear usage guidelines and disclaimers.

---

# 9. Implementation Notes (Internal)

This section describes how a development team should structure the initial MVP and subsequent versions.

---

## 9.1 Git Repository Structure (Recommended)

```
/ci-project
   /docs
      CI_DESIGN_DOCUMENT_V1.0_INTERNAL.md
   /core
      /metrics
      /normalization
      /scoring
   /subsystems
      /background
      /watch
      /screen
      /monitor
   /data-ingestion
   /api
   /ui
```

This structure makes each subsystem an independent module.

---

## 9.2 Minimum Viable Formula Architecture

The MVP should include:
- donor metrics
- one normalized metric
- simple aggregation
- minimal UI displaying CI-Core

This establishes the first functional prototype needed for IP recognition.

---

## 9.3 API Interaction Patterns

### Pull APIs
- scheduled cron jobs
- periodic refreshing
- daily donor/asset updates

### Push APIs (where supported)
- incoming event notifications
- entity updates

---

## 9.4 Versioning Strategy

- **v1.x:** metric architecture and core logic
- **v2.x:** subsystem dashboards
- **v3.x:** advanced graph analytics
- **v4.x:** machine-assisted recommendations

Version locking prevents later disputes over “what was invented when.”

---

## 9.5 Engineering Notes

- use type-safe models (Java/Kotlin recommended)
- separate domain objects from metric-calculation logic
- maintain full test coverage for each metric
- treat the scoring engine as a pure function of inputs

This ensures reproducibility for legal defensibility.

---

# 10. Roadmap

This section defines the strategic milestones for the CI platform.  
It supports IP claims by documenting the intended evolution of the system, demonstrating that the subsystems and advanced features were part of the foundational vision.

---

## 10.1 Phase 1 — MVP (Q1–Q2)

### Objectives
- Implement core ingestion pipeline
- Deliver one functioning normalized metric (Donor Metrics recommended)
- Compute preliminary CI-Core output
- Implement basic UI
- Deploy to private Git repo

### Outcomes
- Establishes “working prototype” status for IP purposes
- Creates foundation for investor presentations
- Demonstrates feasibility of normalized scoring logic

---

## 10.2 Phase 2 — Core Expansion (Q2–Q3)

### Objectives
- Complete all 11 CI-Core metrics
- Implement normalization strategy
- Apply final weight classes
- Build full CI-Core scoring engine
- Publish developer documentation

### Outcomes
- Fully functional CI-Core
- Score reproducibility
- Initial outreach to partners

---

## 10.3 Phase 3 — Subsystem Activation (Q3–Q4)

### CI-Background
- static due-diligence report generator
- entity integrity checks

### CI-Screen
- lightweight hiring/appointment vetting
- R/Y/G output

### CI-Watch
- scheduled monitoring
- alerting framework

### CI-Monitor
- long-term drift visualization

### Outcomes
- CI becomes a **platform** with multiple product lines
- Strong defensibility in trademark filings for subsystem names

---

## 10.4 Phase 4 — Dashboard & Visualization Layer (Q4–Q1 Next Year)

### Objectives
- CI-Watch dashboard
- CI-Monitor drift graphs
- Profile pages for individuals
- Alert explanations and drilldowns

---

## 10.5 Phase 5 — Advanced Analytics (Future)

### Possible features
- cluster-based risk recommendations
- patterns-of-life style analysis
- long-term donor ecosystem predictions
- graph embeddings for network risk

These are optional but forward-looking.

---

# 11. Appendices

This appendix documents underlying structures, schemas, and pseudocode patterns.  
These are not full implementations but serve to further solidify the architectural originality of the CI platform.

---

# 11.1 Entity Definitions

### **Subject**
```
id  
name  
aliases[]  
positions[]  
disclosures[]  
network_nodes[]  
properties[]  
legal_events[]  
donor_events[]  
lobby_events[]  
sentiment_timeseries[]  
```

### **DonorEvent**
```
donor_name  
amount  
date  
source  
cluster_id  
```

### **PropertyRecord**
```
parcel_id  
purchase_price  
purchase_date  
owner_entity  
previous_owner  
```

### **LegalEvent**
```
case_id  
type  
severity  
date  
status  
```

---

# 11.2 Example Metric Pseudocode (High-Level)

### 11.2.1 Donor Concentration (Raw Score)
```
function donorConcentration(events):
    donors = extractUniqueDonors(events)
    total = sum(events.amount)
    hhi = 0
    for donor in donors:
        share = sum(donor.amount) / total
        hhi += share * share
    return hhi
```

### 11.2.2 Real Estate Velocity Heuristic
```
function realEstateVelocity(records):
    sorted = sortByDate(records)
    flips = 0
    for i in 0..len(sorted)-2:
        if sorted[i+1].purchase_date - sorted[i].purchase_date < threshold:
            flips += 1
    return flips
```

### 11.2.3 Investigative Pressure Index Kernel
```
function investigativePressure(mediaEvents):
    velocity = derivative(mediaEvents.count_per_day)
    acceleration = derivative(velocity)
    score = weightedSum(velocity, acceleration)
    return score
```

These examples show the computation patterns without revealing full formulas.

---

# 11.3 Normalization Example Pattern
```
function normalize(rawValue, distribution):
    z = (rawValue - distribution.mean) / distribution.std
    bounded = 1 / (1 + exp(-z))     // logistic compression
    return bounded * 100
```

---

# 11.4 ERD (Textual Representation)

### High-Level Entity Relationship Diagram
```
Subject
   |-- DonorEvent (many)
   |-- PropertyRecord (many)
   |-- LegalEvent (many)
   |-- LobbyEvent (many)
   |-- SentimentSignal (many)
   |-- NetworkNode (many)
```

This establishes the relational architecture.

---

# 11.5 Risk Class Definitions

### **High-Impact Metrics**
- Wealth Anomaly
- Transactional Appointments
- Policy Misalignment Risk

### **Mid-Impact Metrics**
- Donor Metrics
- Legal Irregularities
- Social Ecosystem Alignment

### **Low-Impact Metrics**
- Personal Conduct Anomalies
- Casino License Heuristic

These definitions support consistent scoring and interpretation.

---

# 12. Donor Metrics MVP Prototype (V1.0)

### 12.1 Purpose

The Donor Metrics MVP prototype provides the first executable implementation of a CI metric. It demonstrates the full pipeline from structured input, through normalization and weighted scoring, to human-readable output. This prototype establishes the initial reduction-to-practice of the CI architecture and forms the foundation for implementing additional metrics.

---

### 12.2 Implementation Overview

The MVP is implemented as a minimal Java/Gradle console application with the following components:

- **Language / Build System:** Java with Gradle (Kotlin DSL)
- **Package Root:** `com.ci`
- **Key Classes:**
    - `com.ci.metrics.DonorMetricsRaw`
    - `com.ci.metrics.DonorMetricsScorer`
    - `com.ci.mvp.DonorMetricsMvpRunner`
- **Sample Input File:** `src/main/resources/donor_metrics_sample.json`

Execution flow:

1. Load donor-related JSON data from the resources directory.
2. Deserialize JSON into a typed Java object (`DonorMetricsRaw`).
3. Normalize and weight donor-related features.
4. Compute:
    - a 0–1 normalized donor risk, and
    - a 0–100 Donor Metrics component score.
5. Print the results to the console for inspection.

---

### 12.3 Input Data Model

The `DonorMetricsRaw` class represents the raw donor-related features used in the MVP:

- **donorConcentrationHHI (double)**  
  Herfindahl–Hirschman Index value between 0 and 10,000. Higher values indicate stronger concentration among fewer donors.

- **donationEvents (int)**  
  Total number of recorded donation events over a defined period.

- **donorClusterScore (double)**  
  Pre-normalized 0–1 score representing donor clustering by geography, industry, or other shared attributes.

Sample JSON used by the MVP:

    {
      "donorConcentrationHHI": 7200,
      "donationEvents": 340,
      "donorClusterScore": 0.82
    }

This file is stored at:

- `src/main/resources/donor_metrics_sample.json`

---

### 12.4 Normalization and Scoring Logic

The `DonorMetricsScorer` performs feature scaling and weighted aggregation.

**Feature scaling (all values clamped to [0, 1]):**

- `hhiRisk = clamp(donorConcentrationHHI / 10000)`
- `eventsRisk = clamp(donationEvents / 100)`
- `clusterRisk = clamp(donorClusterScore)`

**Weighted aggregation formula:**

    donorRisk_0to1 =
        0.50 * hhiRisk +
        0.30 * clusterRisk +
        0.20 * eventsRisk

The final donor risk value `donorRisk_0to1` is clamped to the range [0, 1].

**Score conversion:**

- `donorScore_0to100 = round(donorRisk_0to1 * 100)`

This produces the final **Donor Metrics CI component score** on a 0–100 scale.

---

### 12.5 Runtime Behavior

`DonorMetricsMvpRunner` performs the following at runtime:

1. Loads `donor_metrics_sample.json` from the classpath.
2. Uses Jackson’s `ObjectMapper` to deserialize the JSON into a `DonorMetricsRaw` instance.
3. Passes the object into `DonorMetricsScorer` to compute the normalized risk and component score.
4. Prints the results to standard output.

Example console output:

    === Donor Metrics MVP (JSON) ===
    Raw input: DonorMetricsRaw{donorConcentrationHHI=7200.0, donationEvents=340, donorClusterScore=0.82}
    Normalized donor risk (0–1): 0.8xx
    Donor Metrics CI component score (0–100): 8x

This confirms the end-to-end operation of the MVP pipeline.

---

### 12.6 Architectural Significance

The Donor Metrics MVP:

- Demonstrates a complete, functioning CI metric pipeline.
- Establishes the pattern for implementing the remaining CI metrics.
- Provides a concrete example of raw feature ingestion, normalization, weighting, and scoring.
- Creates a traceable link between the design document and runnable code.
- Lays the groundwork for real data integrations (e.g., FEC APIs, third-party datasets) in future versions.

---

### 12.7 IP and Versioning Note

The Donor Metrics MVP prototype has been committed and timestamped in the CI repository alongside this design document. Its presence:

- Demonstrates reduction-to-practice of the Donor Metrics concept.
- Provides cryptographically verifiable authorship and priority via Git history.
- Establishes the CI system as an identifiable intellectual property asset.
- Forms part of the canonical V1.0 architecture and implementation baseline.

This section completes the V1.0 documentation of the Donor Metrics component and provides the reference implementation pattern for additional metric modules.

---

# 13 Disclaimer

This design document is not intended to produce public policy judgments or legal determinations.  
It describes an analytical risk-scoring system using publicly available information and is intended for research, editorial, compliance-support, and investigative-preparation purposes only.

---

# End of CI_DESIGN_DOCUMENT_V1.0.md
**Author: John Forrester**  
**Status: Locked for IP Protection**  
**Version: 1.0**






