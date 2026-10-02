# Mayank Raj

**ML Security Researcher** · Ph.D. Student in Computer Science, University of Illinois Chicago · Systems and Internet Security Lab, advised by Prof. V.N. Venkatakrishnan

I build ML systems that move cyber defense from **reactive detection** to **proactive prediction and decision**. My Ph.D. work focuses on the security of **LLM agents**, including prompt injection.

📍 Chicago, IL, USA · ✉️ [raj02mayank@gmail.com](mailto:raj02mayank@gmail.com) · 🌐 [mayank02raj.github.io](https://mayank02raj.github.io) · 💼 [LinkedIn](https://www.linkedin.com/in/mayank02raj) · 🆔 [ORCID](https://orcid.org/0009-0001-2341-9002)

![Badge: UIC PhD](https://img.shields.io/badge/Ph.D.-UIC%20Computer%20Science-0A1830?style=flat-square&labelColor=D50032) ![Badge: DoD Research](https://img.shields.io/badge/Research-DoD%20W911NF--22--2--0160-0A1830?style=flat-square&labelColor=1F4E79) ![Badge: West Point Collab](https://img.shields.io/badge/Collaboration-U.S.%20Military%20Academy-0A1830?style=flat-square&labelColor=1F4E79) ![Badge: NCAE 2026](https://img.shields.io/badge/NCAE%202026-%231%20National%20Score%20(140%2B%20teams)-2DD4A8?style=flat-square&labelColor=0A1830) ![Badge: Papers](https://img.shields.io/badge/First--Author%20Papers-4-4FA3FF?style=flat-square&labelColor=0A1830)

---

## 🔭 Now

- **Ph.D. in Computer Science, UIC** (Fall 2026–present): security of LLM agents and prompt injection
- **ARA-OSID journal paper** in preparation for **ACM TOPS**
- Working toward **OSCP**

---

## 📄 Research & Publications

Four first-author papers (SECRYPT 2026, a DSN 2026 workshop paper, and two arXiv preprints) plus a journal paper in preparation, all from DoD-funded research (Cooperative Agreement W911NF-22-2-0160) with the U.S. Military Academy at West Point. Together they answer two linked questions for network defense:

> **"What will the attacker do next?"** → **"Given that, what should the defender do?"**

### MITRE ATT&CK-Based Attack Chain Prediction Using Hybrid LSTM-Markov Models for Cybersecurity Risk Assessment · **SECRYPT 2026, published**
Hybrid LSTM-Markov framework that forecasts multi-stage adversary progressions against MITRE ATT&CK. Given an observed prefix (e.g., `T1566.001 → T1059 → T1003`), it generates risk-ranked continuations via constrained beam search. **86% next-step accuracy**, **26,051 forecasts** at **<0.2 sec** latency. Trained on 4,849 MITRE campaign chains and 8,437 real-world intrusion traces.
→ Repo: [`ATTACK-Chain-Prediction`](https://github.com/mayank02raj/ATTACK-Chain-Prediction)

### From Threat Intelligence to Decision Theory: ATT&CK-Derived Utility Functions for Adversarial Risk Analysis in NIDS · **DSN 2026 Workshop, accepted**
Adds an Adversarial Risk Analysis (ARA-OSID) layer that selects the **defender-optimal response policy** across the full threat landscape. **First derivation of all 10 ARA utility-function parameters** from structured MITRE ATT&CK v16 metadata. Validated across **201 techniques**, **143 threat groups**, and **33 campaigns**.

### ARA-OSID Journal Paper · **in preparation for ACM TOPS**
Full journal treatment of the ARA-OSID framework, extending the DSN workshop paper with complete validation and sensitivity analysis.

### M.S. Thesis · **UMass Dartmouth, 2026, open access**
*From Threat Intelligence to Decision Theory: Empirically Grounded Utility Functions for Adversarial Risk Analysis in Network Intrusion Detection.* Ties attack chain prediction and ARA-OSID into one integrated framework.
→ [doi.org/10.62791/20632](https://doi.org/10.62791/20632)

### Earlier parts of the program (preprints)

- **Categorical Robustness Assessment and Model Evaluation for ML-Based NIDS** ([arXiv:2606.12075](https://arxiv.org/abs/2606.12075)): CNN retains **95.5%** accuracy while Random Forest collapses to **26.8%** under ε=0.01 FGSM on ACI-IoT-2023, a **68.66-pp gap** that benchmark accuracy alone does not predict. → [`Robustness-of-NIDS`](https://github.com/mayank02raj/Robustness-of-NIDS)
- **Synthetic Network Packet Generation through Statistical Learning and Genetic Algorithms** ([arXiv:2606.20864](https://arxiv.org/abs/2606.20864)): **200× amplification** of a 5-sample ARP Spoofing class with **<2.5% anomaly rate** against independent validators. → [`Synthetic-Network-Packet-Generation`](https://github.com/mayank02raj/Synthetic-Network-Packet-Generation)

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

## 🏆 Recognition & Service

- **1st place, highest national score**, 2026 NCAE Cyber Games (Northeast 2 Region, 140+ teams)
- **Reviewer:** IEEE MILCOM 2026 (AI/ML for Communication and Networking track) · IEEE GLOBECOM 2026 (workshop) · IEEE MILCOM 2025 (WS07 workshop)
- **Technical Program Committee:** DSN 2026 Workshop on Dependable and Secure Autonomous Systems
- **Certifications:** ISC2 Certified in Cybersecurity (CC), 2025 · OSCP (in progress)
- **Teaching:** GTA for CIS-190 Procedural Programming and CIS-552 Database Design, UMass Dartmouth
- **Membership:** IEEE Student Member, Communications Society

---

## 🎓 Background

- **Ph.D. Computer Science**, University of Illinois Chicago · Fall 2026–present
- **M.S. Data Science (Thesis Track)**, UMass Dartmouth · GPA 3.6/4.0 · 2026
  - Graduate Research Assistant on DoD-funded research with the U.S. Military Academy at West Point
  - Thesis defended August 2026 · [open access](https://doi.org/10.62791/20632)
- **B.Tech. Mechanical Engineering**, Christ University, Bengaluru
- **3.5+ years industry experience:** Data Scientist / Software Engineer at Eklavya Estate (Bengaluru), with ETL pipelines on 500K+ records, ARIMA + LSTM forecasting across 15+ markets, and AWS microservices at 10K+ concurrent users; ML engineering intern at Hindustan Aeronautics Limited (HAL) on aerospace systems

---

**Open to research collaborations and Summer 2027 research internships** in ML security, LLM agent security, and threat detection.
