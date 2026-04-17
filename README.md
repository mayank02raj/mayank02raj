<h1 align="center">Mayank Raj</h1>

<p align="center">
  <strong>ML Security Researcher</strong> · Predictive Cyber Defense · Adversarial ML for NIDS<br>
  M.S. Data Science @ UMass Dartmouth · Graduating May 2026
</p>

<p align="center">
  <a href="https://mayank02raj.github.io"><img src="https://img.shields.io/badge/Portfolio-mayank02raj.github.io-1F6FEB?style=flat-square&logo=github" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/mayank02raj"><img src="https://img.shields.io/badge/LinkedIn-mayank02raj-0A66C2?style=flat-square&logo=linkedin" alt="LinkedIn"></a>
  <a href="mailto:raj02mayank@gmail.com"><img src="https://img.shields.io/badge/Email-raj02mayank%40gmail.com-D44638?style=flat-square&logo=gmail" alt="Email"></a>
  <img src="https://img.shields.io/badge/Work%20Auth-F--1%20STEM%20OPT-2EA44F?style=flat-square" alt="Work Authorization">
</p>

-----

## About

I build ML systems that move cyber defense from **reactive detection to proactive prediction**. My flagship research uses hybrid LSTM-Markov models to forecast multi-stage adversary progressions against the MITRE ATT&CK framework — anticipating an attacker’s next move with 86% accuracy from three observed steps, and scoring each predicted continuation on a continuous 0–10 risk scale that SOC teams can act on.

The same research agenda extends into measuring where existing ML-based detectors fail under adversarial pressure, generating the synthetic training data needed to fix them, and quantifying open-set uncertainty in intrusion detection. Four first-author papers currently under review, all supported by a DoD Cooperative Agreement with the **U.S. Military Academy at West Point**.

Currently a Graduate Research Assistant at UMass Dartmouth working with **Dr. Gokhan Kul**. Before the MS, 3+ years as a Data Scientist and Software Engineer at Eklavya Estate (Bengaluru), shipping ETL pipelines, time-series forecasting, and AWS microservices for production use — which is why the research I do is grounded in deployable systems, not just benchmarks.

**Graduating May 2026, thesis defense August 2026. Open to cybersecurity research-scientist, threat-detection-engineering, and ML-engineer roles in the US.**

-----

## Most Recent Research: ATT&CK-based Attack Chain Prediction

A hybrid LSTM-Markov framework for forecasting multi-stage adversary progressions against MITRE ATT&CK. Given three observed techniques from a defender’s telemetry, the pipeline generates risk-ranked predictions of what the attacker will do next:

```
 Observed prefix:                        Top predicted continuation:
 ───────────────                         ──────────────────────────
 T1566.001  Spearphishing Attachment     Lateral Movement →
 T1059      PowerShell Execution     →   Data Staging →
 T1003      OS Credential Dumping        Exfiltration over C2
                                         Risk: 9.4 / 10
```

- **86% next-step prediction accuracy** across three training regimes
- **Pearson r = 0.76** and **Spearman ρ = 0.81** correlation against CISA NCISS severity (80/20 scenario)
- **42.3% real-world transition coverage** across **26,051 risk-ranked forecasts** from 800 seed prefixes
- Inference latency **under 0.2 seconds per prefix** — SOC-workflow compatible
- Formal 0–10 risk model integrating EPSS, CAPEC, LSTM confidence, CISA KEV, D3FEND coverage, and OCTAVE-based organizational impact

**Under review at SECRYPT 2026.** Code, dataset, trained models, and beam-generated forecasts:
**[`github.com/mayank02raj/ATTACK-Chain-Prediction`](https://github.com/mayank02raj/ATTACK-Chain-Prediction)**

-----

## Supporting Research

Three additional first-author papers that extend the research agenda across the full defensive stack. All DoD-funded.

|Paper                                                                                  |Venue                           |Core Finding                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Categorical Robustness Assessment for ML-based NIDS**                                |IEEE Access (under review)      |The *False Champion Problem*: Random Forest collapses from 99.98% → 26.8% under FGSM at ε=0.01, while CNN retains 95.5%. Architecture beats hyperparameters for adversarial deployment.|
|**Synthetic Network Packet Generation via Statistical Learning and Genetic Algorithms**|ICCCN 2026 (under review)       |Constraint-enforcing generation that passes independent validators across all 12 ACI-IoT-2023 categories. 200× amplification of a 5-sample ARP Spoofing class where SMOTE fails.       |
|**Adversarial Risk Analysis for Open-Set Intrusion Detection**                         |DSN 2026 Workshop (under review)|ARA utility-function framework for open-set detection under adversarial uncertainty.                                                                                                   |

Together, the four papers tell one story: **measure where detectors fail** (Robustness), **generate the data to fix them** (Synthetic Packet Generation), **predict what the adversary will do next** (ATT&CK Chain Prediction — the flagship), and **quantify uncertainty when facing the unknown** (ARA-OSID).

-----

## Highlights

- 🏆 **1st place** at the **2026 NCAE Cyber Games** (Northeast 2 region) — highest overall score among 140 national teams. Live SOC work with Splunk, Corelight, MITRE ATT&CK Navigator, and real-time hardening on Rocky Linux.
- 🎓 **IEEE MILCOM 2025 reviewer** · **DSN 2026 Workshop TPC member** · **IEEE Communications Society member**
- 🔬 **DoD-funded research** — 2.5+ years on the Adversarial Risk Analysis for Cybersecurity project (Cooperative Agreement W911NF-22-2-0160) with West Point
- 🏢 **3+ years industry experience** before the MS — Data Scientist and Software Engineer at Eklavya Estate (Bengaluru), shipping ETL pipelines, time-series forecasting, and AWS microservices
- 🛡️ **ISC2 Certified in Cybersecurity (CC)** · **OSCP in progress** (April–August 2026)
- 🎤 **CTF team lead**, organizer of the OWASP Juice Shop CTF for the Cyber Secure Computing Club at UMass Dartmouth

-----

## Portfolio

Six production-shaped repositories. **Pinned below in recommended reading order** — each README includes architecture diagrams, reproducibility notes, and a “skills mapped to job postings” section.

### Flagship: Predictive Security Research

**[`ATTACK-Chain-Prediction`](https://github.com/mayank02raj/ATTACK-Chain-Prediction)** · **SECRYPT 2026 submission**

> Hybrid LSTM-Markov attack-chain forecasting. Learns from 4,849 MITRE campaign chains + 8,437 real intrusion traces (Unit42 + MITRE Attack Flow). Generates 26,051 risk-ranked multi-step attack futures via constrained beam search. 86% next-step accuracy, 0.76 Pearson correlation with NCISS severity, <0.2 sec per prefix. Integrates EPSS, CAPEC, CISA KEV, D3FEND, and OCTAVE into a formal 0–10 risk model.

### Supporting Research

**[`Robustness-of-NIDS`](https://github.com/mayank02raj/Robustness-of-NIDS)** · **IEEE Access submission**

> Adversarial robustness evaluation framework. CNN vs LSTM vs Random Forest on ACI-IoT-2023 (1.23M packets) under FGSM, PGD, and CLEVER certification. Formalizes the **False Champion Problem**: Random Forest wins clean benchmarks (99.98%) but collapses to 26.8% at ε=0.01.

**[`Synthetic-Network-Packet-Generation`](https://github.com/mayank02raj/Synthetic-Network-Packet-Generation)** · **ICCCN 2026 submission**

> Constraint-enforcing synthetic IoT packet generation. Statistical learning (PCA + dual OCSVM/IF gating, ~1,091 pkts/sec) and a genetic algorithm (composite fitness, 0.62% anomaly rate). Amplifies the 5-sample ARP Spoofing class by 200×. All 12 ACI-IoT-2023 categories pass independent validators.

### Detection & SOC Infrastructure

**[`SOC-home-lab`](https://github.com/mayank02raj/SOC-home-lab)** · Python 65% · Jupyter 25%

> Production-shaped 11-service Dockerized SOC with Wazuh SIEM, Suricata IDS, TheHive, Cortex, Grafana, and Prometheus. Detection-as-code with Sigma rules, CI-validated unit tests, a Sigma-to-Wazuh compiler, an 8-stage MITRE ATT&CK adversary emulation script, and a threat-hunting Jupyter notebook.

**[`ATTACK-Coverage-Dashboard`](https://github.com/mayank02raj/ATTACK-Coverage-Dashboard)** · Python 97%

> MITRE ATT&CK detection coverage analytics. Ingests Sigma, Wazuh XML, and JSON rules; produces naive + data-source-weighted coverage scores across 130+ threat actors; exports ATT&CK Navigator JSON and PDF reports. 7-page Streamlit UI with real Enterprise-matrix heatmap, SQLite backend, full CI.

### ML for Security

**[`Phishing-URL-Detector`](https://github.com/mayank02raj/Phishing-URL-Detector)** · Python 92%

> Production-shaped ML service. XGBoost on 42 engineered features + CharCNN on raw URLs, FastAPI with SHAP per-request explanations, PSI drift monitoring, Prometheus metrics, multi-stage Dockerfile. ~97% accuracy at <1ms CPU inference.

-----

## Tech

**ML & Deep Learning**
`PyTorch` · `scikit-learn` · `XGBoost` · `SHAP` · `Adversarial Robustness Toolbox` · `HuggingFace Transformers` · `MLflow`

**Cybersecurity Stack**
`MITRE ATT&CK` · `D3FEND` · `Sigma Rules` · `Wazuh` · `Suricata` · `Splunk` · `Corelight` · `TheHive` · `Cortex` · `STIX 2.x` · `EPSS` · `CAPEC` · `CISA KEV` · `Metasploit` · `Burp Suite`

**Backend & Infrastructure**
`FastAPI` · `Docker` · `Kubernetes` · `AWS (EC2, S3, Lambda)` · `SQLite` · `PostgreSQL` · `Redis` · `Prometheus` · `Grafana` · `GitHub Actions`

**Languages**
`Python` · `Bash` · `SQL` · `C/C++` (academic) · `JavaScript` (academic)

-----

## Collaborators

|                                                                                                               |                                 |
|---------------------------------------------------------------------------------------------------------------|---------------------------------|
|**Dr. Gokhan Kul** — Advisor · Associate Director of Cybersecurity Center, UMass Dartmouth                     |[UMassD](https://www.umassd.edu) |
|**Dr. Nathaniel D. Bastian** — Deputy Director of Robotics Research Center, U.S. Military Academy at West Point|[USMA](https://www.westpoint.edu)|
|**Dr. Lance Fiondella** — Director of Cybersecurity Center, UMass Dartmouth (NSA/DHS-designated CAE-R)         |[UMassD](https://www.umassd.edu) |

Research at UMass Dartmouth is conducted at the [Cybersecurity Center](https://www.umassd.edu/cybersecurity/), an **NSA/DHS-designated Center of Academic Excellence in Cyber Research** (CAE-R).

-----

## Professional Memberships & Service

- **IEEE Communications Society** (ComSoc) — Student Member
- **IEEE MILCOM 2025** — Technical Paper Reviewer
- **DSN 2026 Workshop** — Technical Program Committee Member

-----

## Work Authorization

**F-1 STEM OPT eligible** — 36 months of work authorization post-graduation (May 2026 – August 2029). **E-Verify compatible. No sponsorship required through August 2029.**

Open to cybersecurity research-scientist, threat-detection-engineering, ML-engineer, and security-research roles across the Boston / NYC / DC corridor, and nationwide for the right fit.

-----

## Contact

The best way to reach me is **email** or a **LinkedIn DM**:

- ✉️ [raj02mayank@gmail.com](mailto:raj02mayank@gmail.com)
- 💼 [linkedin.com/in/mayank02raj](https://linkedin.com/in/mayank02raj)
- 🌐 [mayank02raj.github.io](https://mayank02raj.github.io)

For research inquiries (paper preprints, collaboration, reproducibility questions), email is preferred. Preprints for the four papers above are available on request pending institutional review.

<p align="center"><em>Last updated: April 2026</em></p>
