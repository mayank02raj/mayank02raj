# Mayank Raj

**ML Security Researcher** · Graduate Research Assistant, UMass Dartmouth × U.S. Military Academy at West Point

I build ML systems that move cyber defense from **reactive detection** to **proactive prediction and decision**.

📍 Dartmouth, MA · ✉️ [raj02mayank@gmail.com](mailto:raj02mayank@gmail.com) · 🌐 [mayank02raj.github.io](https://mayank02raj.github.io) · 💼 [LinkedIn](https://www.linkedin.com/in/mayank02raj)

![Badge — DoD Research](https://img.shields.io/badge/Research-DoD%20W911NF--22--2--0160-0A1830?style=flat-square&labelColor=1F4E79) ![Badge — West Point Collab](https://img.shields.io/badge/Collaboration-U.S.%20Military%20Academy-0A1830?style=flat-square&labelColor=1F4E79) ![Badge — NCAE 2026](https://img.shields.io/badge/NCAE%202026-%231%20National%20Score%20(140%20teams)-2DD4A8?style=flat-square&labelColor=0A1830) ![Badge — Papers](https://img.shields.io/badge/First--Author%20Papers-4%20(1%20Accepted%2C%203%20Under%20Review)-4FA3FF?style=flat-square&labelColor=0A1830)

---

## 📄 Research & Publications

Four first-author papers (1 accepted, 3 under review), all supported by DoD Cooperative Agreement W911NF-22-2-0160 in collaboration with the U.S. Military Academy at West Point. The program builds a full pipeline from **robustness evaluation** → **data augmentation** → **attack prediction** → **optimal defense selection**.

### MITRE ATT&CK-Based Attack Chain Prediction Using Hybrid LSTM-Markov Models for Cybersecurity Risk Assessment (SECRYPT 2026, under review)
Hybrid LSTM-Markov framework that forecasts multi-stage adversary progressions against MITRE ATT&CK. Given an observed prefix (e.g., `T1566.001 → T1059 → T1003`), generates risk-ranked continuations via constrained beam search. **86% next-step accuracy**, **26,051 forecasts** at **<0.2 sec** latency. Trained on 4,849 MITRE campaign chains + 8,437 real-world intrusion traces.
→ Repo: [`ATTACK-Chain-Prediction`](https://github.com/mayank02raj/ATTACK-Chain-Prediction)

### From Threat Intelligence to Decision Theory: ATT&CK-Derived Utility Functions for Adversarial Risk Analysis in NIDS (DSN 2026 Workshop, ACCEPTED)
Decision-theoretic extension that adds an Adversarial Risk Analysis (ARA-OSID) layer selecting **defender-optimal response policy** across the full threat landscape. **First-ever derivation of all 10 ARA utility-function parameters** from structured MITRE ATT&CK v16 metadata. Validated across **201 techniques**, **143 threat groups**, and **33 campaigns**.
→ The two parts answer complementary questions: **"What will the attacker do?"** and **"Given that, what should the defender do?"**

### Categorical Robustness Assessment and Model Evaluation for Machine Learning-Based Network Intrusion Detection Systems (IEEE Access, under review)
CNN retains **95.5%** accuracy vs Random Forest collapsing to **26.8%** under ε=0.01 FGSM on ACI-IoT-2023, exposing a **68.66-pp gap** that benchmark accuracy alone cannot predict.
→ Repo: [`Robustness-of-NIDS`](https://github.com/mayank02raj/Robustness-of-NIDS)

### Synthetic Network Packet Generation through Statistical Learning and Genetic Algorithms (ICCCN 2026, under review)
Constraint-enforcing generator combining statistical learning and genetic algorithms. Achieves **200× amplification** of a 5-sample ARP Spoofing class with **<2.5% anomaly rate** against independent validators, enabling privacy-preserving security testing.
→ Repo: [`Synthetic-Network-Packet-Generation`](https://github.com/mayank02raj/Synthetic-Network-Packet-Generation)

---

## 💻 Production-Shaped Open Source

### Security & Detection

| Repo | Stack | What it demonstrates |
|---|---|---|
| [`SOC-home-lab`](https://github.com/mayank02raj/SOC-home-lab) | Wazuh, Suricata, TheHive, Cortex, Grafana, Prometheus, Docker Compose | 11-service Dockerized SOC with 9 authored Sigma rules (pytest CI), custom Sigma-to-Wazuh compiler, 8-stage MITRE ATT&CK adversary emulation covering 91.3% of the kill chain |
| [`ATTACK-Coverage-Dashboard`](https://github.com/mayank02raj/ATTACK-Coverage-Dashboard) | Streamlit, SQLite, Python | 7-page analytics over MITRE ATT&CK coverage; ingests Sigma / Wazuh-XML / JSON rules; data-source-weighted coverage across 130+ threat actors; exports ATT&CK Navigator JSON + PDF reports |
| [`Phishing-URL-Detector`](https://github.com/mayank02raj/Phishing-URL-Detector) | FastAPI, XGBoost, PyTorch (CharCNN), SHAP, Prometheus, Docker | Production-shaped ML service: XGBoost on 42 engineered features + CharCNN on raw URL characters; per-request SHAP explanations, PSI drift monitoring; ~97% accuracy at <1ms CPU inference |
| [`network-traffic-anomaly-visualizer`](https://github.com/mayank02raj/network-traffic-anomaly-visualizer) | Scapy, Plotly, Docker | Packet capture with Z-score/IQR anomaly detection; per-source port scan detection via Shannon entropy; interactive HTML dashboards; streaming mode for long captures |
| [`honeypot-attack-classifier`](https://github.com/mayank02raj/honeypot-attack-classifier) | Paramiko, scikit-learn, Flask, Docker Compose | SSH/HTTP/FTP honeypot with Random Forest session classification; thread-safe rate limiting; webhook alerting; real-time dashboard |
| [`cloud-security-auditor`](https://github.com/mayank02raj/cloud-security-auditor) | Boto3, Moto, Docker | AWS security scanner across 6 service areas against CIS benchmarks; multi-region scanning with retry/backoff; CI-friendly exit codes |

### ML / Data Science

| Repo | Stack | What it demonstrates |
|---|---|---|
| [`llm-hallucination-detector`](https://github.com/mayank02raj/llm-hallucination-detector) | Sentence-Transformers, spaCy, FastAPI, Streamlit | Factual grounding checker (semantic similarity + entity overlap + numerical accuracy), LLM-as-judge bias detection (positional, verbosity, self-enhancement via binomial tests), calibration curves with ECE/MCE; bootstrap CIs on hallucination rates |
| [`adaptive-experimentation-engine`](https://github.com/mayank02raj/adaptive-experimentation-engine) | NumPy, FastAPI, Streamlit | A/B tests with O'Brien-Fleming sequential monitoring, Thompson Sampling (Beta-Bernoulli), contextual bandits (online logistic regression); simulation engine comparing regret across strategies; file-backed state persistence |
| [`ts-foundation-benchmark`](https://github.com/mayank02raj/ts-foundation-benchmark) | PyTorch, statsmodels, XGBoost, Chronos | Benchmark comparing ARIMA, LSTM (early stopping + val split), XGBoost (lag features + cyclical encoding) against foundation models; few-shot learning curves at varying context lengths |

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
