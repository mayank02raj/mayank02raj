# Mayank Raj

**ML Security Researcher** · Graduate Research Assistant, UMass Dartmouth × U.S. Military Academy at West Point

I build ML systems that move cyber defense from **reactive detection** to **proactive prediction and decision**.

📍 Dartmouth, MA · ✉️ [raj02mayank@gmail.com](mailto:raj02mayank@gmail.com) · 🌐 [mayank02raj.github.io](https://mayank02raj.github.io) · 💼 [LinkedIn](https://www.linkedin.com/in/mayank02raj)

![Badge — DoD Research](https://img.shields.io/badge/Research-DoD%20W911NF--22--2--0160-0A1830?style=flat-square&labelColor=1F4E79) ![Badge — West Point Collab](https://img.shields.io/badge/Collaboration-U.S.%20Military%20Academy-0A1830?style=flat-square&labelColor=1F4E79) ![Badge — NCAE 2026](https://img.shields.io/badge/NCAE%202026-%231%20National%20Score%20(140%20teams)-2DD4A8?style=flat-square&labelColor=0A1830) ![Badge — Papers](https://img.shields.io/badge/First--Author%20Papers-4%20Under%20Review-4FA3FF?style=flat-square&labelColor=0A1830)

---

## 🎯 Recent Research

A two-part program on **predictive cyber defense with empirical decision theory**. Both parts submitted, both supported by DoD Cooperative Agreement W911NF-22-2-0160 in collaboration with the U.S. Military Academy at West Point.

### Part 1 — Attack Chain Prediction (SECRYPT 2026, under review)
Hybrid LSTM-Markov framework that forecasts multi-stage adversary progressions against MITRE ATT&CK. Given an observed attack prefix (e.g., `T1566.001 → T1059 → T1003`), the system generates risk-ranked continuations via constrained beam search.

- **86% next-step accuracy**, Pearson **r=0.76** / Spearman **ρ=0.81** against CISA NCISS severity scoring
- **26,051 risk-ranked forecasts** at **<0.2 sec** inference latency per prefix
- Trained on 4,849 MITRE campaign chains + 8,437 real-world intrusion traces (Unit42 + MITRE Attack Flow)
- Formal 0–10 risk model integrates EPSS, CAPEC, CISA KEV, D3FEND coverage, OCTAVE impact

→ Repo: [`ATTACK-Chain-Prediction`](https://github.com/mayank02raj/ATTACK-Chain-Prediction)

### Part 2 — ATT&CK-Derived Decision Theory (DSN 2026 Workshop, under review)
Decision-theoretic extension of Part 1. Takes the same pipeline's data structures and adds an Adversarial Risk Analysis (ARA-OSID) layer that selects **defender-optimal response policy** `r*` across the full threat landscape.

- **First-ever derivation of all 10 ARA utility-function parameters** from structured MITRE ATT&CK v16 metadata — no assumed values
- Joint attacker-defender model with Monte Carlo integration (N=10,000) over Beta-distributed detection probabilities
- Validated across **201 techniques**, **143 threat groups**, and **33 campaigns**
- Attacker utility `ψ_A` built from technique permissions, D3FEND coverage, kill-chain position, NCISS benefit
- Defender utility `ψ_r` built from group frequency, severity-weighted detection gaps, evasion sub-technique counts, mitigation portfolio size

→ The two parts answer complementary questions: **Part 1 asks "what will the attacker do?"** **Part 2 asks "given that, what should the defender do?"**

---

## 🛠️ Supporting Research

Research on the infrastructure the flagship pipeline depends on. Two first-author papers under review.

| Paper | Venue | Contribution | Repo |
|---|---|---|---|
| **The False Champion Problem** — categorical robustness assessment of ML-based NIDS | IEEE Access | CNN retains **95.5%** accuracy vs Random Forest collapsing to **26.8%** under ε=0.01 FGSM on ACI-IoT-2023 (68.66-pp gap) | [Robustness-of-NIDS](https://github.com/mayank02raj/Robustness-of-NIDS) |
| **Constraint-enforcing synthetic packet generation** | ICCCN 2026 | **200× amplification** of a 5-sample ARP Spoofing class with **<2.5%** anomaly rate against independent validators | [Synthetic-Network-Packet-Generation](https://github.com/mayank02raj/Synthetic-Network-Packet-Generation) |

---

## 💻 Production-Shaped Open Source

| Repo | Stack | What it demonstrates |
|---|---|---|
| [`SOC-home-lab`](https://github.com/mayank02raj/SOC-home-lab) | Wazuh, Suricata, TheHive, Cortex, Grafana, Prometheus, Docker Compose | 11-service Dockerized SOC with 9 authored Sigma rules (pytest CI), custom Sigma-to-Wazuh compiler, 8-stage MITRE ATT&CK adversary emulation covering 91.3% of the kill chain |
| [`ATTACK-Coverage-Dashboard`](https://github.com/mayank02raj/ATTACK-Coverage-Dashboard) | Streamlit, SQLite, Python | 7-page analytics over MITRE ATT&CK coverage; ingests Sigma / Wazuh-XML / JSON rules; data-source-weighted coverage across 130+ threat actors; exports ATT&CK Navigator JSON + PDF reports |
| [`Phishing-URL-Detector`](https://github.com/mayank02raj/Phishing-URL-Detector) | FastAPI, XGBoost, PyTorch (CharCNN), SHAP, Prometheus, Docker | Production-shaped ML service: XGBoost on 42 engineered features + CharCNN on raw URL characters; per-request SHAP explanations, PSI drift monitoring; ~97% accuracy at <1ms CPU inference |

---

## 🎓 Background

- **M.S. Data Science (Thesis Track)**, UMass Dartmouth · GPA 3.6/4.0 · expected May 2026
  - *Thesis:* Resilience Engineering of ML-enabled Open-World Recognition for Network Intrusion Detection Systems. Defense August 2026.
- **B.Tech. Mechanical Engineering**, Christ University, Bengaluru
- 4+ years industry ML: Data Scientist / Software Engineer at Eklavya Estate (Bengaluru) — ETL pipelines on 500K+ records, ARIMA + LSTM forecasting across 15+ markets, AWS microservices at 10K+ concurrent users

## 🏆 Competition & Service

- **1st Place** — 2026 NCAE Cyber Games, Northeast 2 Region (highest overall score among 140 national teams)
- **ISC2 Certified in Cybersecurity (CC)** — 2025; **OSCP** in progress, targeting Aug 2026
- Technical Paper Reviewer, **IEEE MILCOM 2025**
- Technical Program Committee, **DSN 2026 Workshop on AI/ML for Cybersecurity**
- Student Member, **IEEE Communications Society**

---

**Open to full-time cybersecurity research-scientist, threat-detection-engineering, and ML-security roles starting Summer 2026.** F-1 STEM OPT eligible — 36 months of work authorization, E-Verify compatible, no sponsorship required through Aug 2029.
