<h1 align="center">Hi, I'm Parv</h1>

<p align="center">
  <b>ML &amp; Backend Engineer</b><br>
  I build the parts of ML systems that don't show up in the accuracy number —<br>
  the pipelines, the services, and the infrastructure that has to hold up under real load.
</p>

<p align="center">
  <a href="https://parvpatel.me"><img src="https://img.shields.io/badge/Portfolio-parvpatel.me-0C0C0C?style=for-the-badge&logo=vercel&logoColor=D7E2EA" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/parvptl/"><img src="https://img.shields.io/badge/LinkedIn-7621B0?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:parv4careers@gmail.com"><img src="https://img.shields.io/badge/Email-B600A8?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://leetcode.com/u/parv_ptl"><img src="https://img.shields.io/badge/LeetCode-BE4C00?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode"></a>
</p>

---

## About

Final-year **B.Tech Data Science** student at **IIT Palakkad** (CGPA 8.34/10, graduating June 2027).

Most of my work sits at the seam between a model and a system that has to serve it — resumable preprocessing pipelines, inference services that validate their inputs, and migrations you can prove are correct rather than assume are. I care about the failure modes as much as the metrics.

**Open to full-time opportunities from 2027.**

---

## What I'm building now

**Hesor — PPG Vital-Sign Monitoring** · *Project Intern, IIT Palakkad · Apr 2026 – Present*

A clinician-facing vitals platform, built end to end:

- Lifted blood-pressure classification out of a PyQt5 research app into a standalone **FastAPI** service — model loaded once at startup, every request validated with Pydantic so malformed IR/RED blocks are rejected before inference.
- Each 5-second block resamples 500 Hz → 125 Hz, runs Chebyshev filtering and peak-onset feature extraction, and returns a three-class result with a finger-detection gate that skips blocks instead of guessing.
- Wrote a **parity harness** that replays identical inputs through both the new service and the original implementation — so the migration was proven numerically equivalent, not assumed.
- Built the **Expo/React Native** client streaming PPG at 500 Hz off an HC-05 sensor over Bluetooth Classic SPP via a custom Kotlin RFCOMM module, buffering in refs and flushing at 10 Hz to hold **60 FPS** on live waveform charts.
- Implemented the signal-processing layer in TypeScript: DC removal, bandpass filtering, AMDF peak detection, and derived metrics (pulse rate, SpO₂, perfusion index, signal quality, HRV).

---

## Featured Projects

### [DualForensics](https://github.com/Parvptl/DualForensics) — Deepfake Detection System
`Python` `PyTorch` `OpenCV` `FastAPI` `Docker` · **AUC 0.9787**

A video pipeline that turned ~7,000 raw videos into ~112,000 cropped faces, tracked by a JSON manifest so interrupted runs resume instead of reprocessing from scratch. Three-step fallback for face extraction (MTCNN → Haar cascade → center crop) so no video is silently dropped, and a 6:1 class imbalance handled with weighted sampling plus a matching weighted loss. Deployed as a Dockerized FastAPI service with upload validation, guaranteed temp-file cleanup, and a health endpoint that returns a clean 503 when weights fail to load.

### [Financial Sentiment Forecasting](https://github.com/Parvptl/Financial-Sentiment-Forecasting) — Entity-Aware Transformers
`Python` `PyTorch` `Transformers` `XGBoost` `LightGBM` · **92%+ accuracy**

An end-to-end pipeline over 25K+ entity-level financial news instances. Fine-tuned DeBERTa-v3 for aspect-based sentiment, then decoupled feature extraction from modeling so the same feature set swaps across 6+ downstream models without retraining the transformer. Leakage-safe temporal aggregation using causally shifted rolling windows, with ablation studies and bootstrap significance testing.

### [Max-Flow Hub](https://github.com/Parvptl/Max-Flow-Hub) — Network Flow Visualizer
`JavaScript` `D3.js` · Ford-Fulkerson, Edmonds-Karp, and Push-Relabel implemented from scratch with step-through animation.

### [NEXUS](https://github.com/Parvptl/NEXUS) — E-Commerce Analytics
`Python` `Streamlit` `Scikit-Learn` · ML pipeline over 100K+ transactions: statistical inference, market basket analysis, customer segmentation.

### [FinTrack](https://github.com/Parvptl/FinTrack) — Investment Management System
`Flask` `PostgreSQL` · Full-stack portfolio management on a normalized schema with role-based access control and ACID-compliant transaction handling.

---

## Experience

**Accenture** — Advanced Engineering Hub Intern · *Bengaluru · May 2026 – Jul 2026*

Contributed to an enterprise **Identity & Access Management** solution, implementing explainable ML pipelines for identity risk scoring and access governance. Engineered risk-scoring features and benchmarked ensemble models (XGBoost, LightGBM) to improve classification accuracy, carrying over feature engineering and explainability techniques from prior transformer-based forecasting work.

---

## Achievements

| | |
|---|---|
| **Amazon ML Summer School 2026** | Selected among 3,000 of 134,421 applicants — **top 2.2%** |
| **Inter IIT Tech Meet 14.0** | **4th nationally** in the Genuity IO Challenge — GAN-based synthetic tabular data generator with topology-preserving losses |
| **Flipkart GRiD 8.0** | Semi-Finalist |
| **Ascent (Synapse) Hackathon** | Finalist — Scaler School of Technology |
| **LeetCode** | 500+ problems solved |

---

## Leadership

**Convener — The Integral Cup** · *Nov 2025 – Present*
Led cross-functional teams to execute a national-level academic competition across 26+ centres (IITs, BITS, IIITs, IISc, ISI), managing logistics, vendors, and operations at scale.

**Fest Coordinator — Petrichor, IIT Palakkad** · *2025 – Jan 2026*
Led end-to-end planning and logistics for IIT Palakkad's flagship inter-college cultural festival; coordinated 30+ events and cross-functional teams.

---

## Tech

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**ML & Deep Learning**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

CNNs · Transformers · Attention Mechanisms · Ensemble Methods · Feature Engineering · Statistical Inference

**Backend & Systems**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)

---

<p align="center">
  <b>Let's talk.</b><br>
  I'm looking for challenging problems where rigorous engineering and ML come together.<br><br>
  <a href="mailto:parv4careers@gmail.com">parv4careers@gmail.com</a> ·
  <a href="https://www.linkedin.com/in/parvptl/">LinkedIn</a> ·
  <a href="https://parvpatel.me">parvpatel.me</a>
</p>
