# Parv Patel

B.Tech Data Science, IIT Palakkad · ML & Backend Engineer

[parvpatel.me](https://parvpatel.me) · [LinkedIn](https://linkedin.com/in/parvptl) · [parv4careers@gmail.com](mailto:parv4careers@gmail.com)

---

### About

I build machine learning systems as production services, not notebooks. Most of my work sits at the boundary between a trained model and the API that has to serve it reliably — input validation, graceful failure, concurrency handling, and the parts of a system that don't show up in an accuracy number but decide whether it survives real traffic.

I'm currently working on explainable AI for enterprise Identity & Access Management at Accenture, and building the backend and mobile app for a clinician-facing vitals monitoring platform at IIT Palakkad.

---

### Selected Work

**[DualForensics](https://github.com/Prish1509/Deep-Fake-Detection)** — Deepfake detection service · [live demo](https://deepfake.parvpatel.me)
A CNN-Transformer video classifier served through a containerized FastAPI microservice. The engineering problem wasn't the model — it was making it survive bad input and concurrent load. Model loading is decoupled from the service lifecycle via a dedicated health check, so a corrupted checkpoint returns a clean `503` instead of taking the service down. Payloads are validated at the edge, temp files are cleaned up in exception-safe blocks, and CPU threading (OMP/MKL) is pinned to stop concurrent requests from contending for cores.
`Python` `PyTorch` `FastAPI` `Docker` `OpenCV`

**[Hesor](https://github.com/Akshat-42/Hesor)** — Real-time vitals dashboard
A React Native app rendering high-frequency physiological waveforms without stuttering the UI. Incoming samples buffer into a mutable ref rather than React state; a single interval flushes and downsamples into state at 10Hz, holding a stable 60 FPS regardless of input rate. Signal processing (bandpass filtering, AMDF peak detection) is written as pure, unit-testable functions, and a FastAPI backend handles blood-pressure classification from 5-second signal blocks.
`React Native` `TypeScript` `FastAPI` `Scikit-Learn`

**[Financial Sentiment Forecasting](https://github.com/Parvptl/Financial_Sentiment_Forecasting)** — Entity-aware transformer pipeline
An end-to-end pipeline over 25K+ entity-level financial news instances. DeBERTa-v3 is fine-tuned for aspect-based sentiment (92%+ accuracy), and its outputs — confidence, entropy, embeddings — are decoupled as reusable features so six-plus downstream forecasting models can be trained without retraining the transformer. Return labels use causally shifted rolling windows to avoid lookahead leakage, validated with bootstrap significance testing.
`Python` `PyTorch` `Transformers` `XGBoost` `LightGBM`

---

### Other Public Repositories

| Repository | What it is |
|---|---|
| [maxflow_visualizer](https://github.com/Parvptl/maxflow_visualizer) · [live](https://flow.parvpatel.me) | Ford-Fulkerson, Edmonds-Karp, and Push-Relabel implemented from scratch, with a D3.js engine animating the Max-Flow Min-Cut theorem |
| [E_Commerce_Analytics](https://github.com/Parvptl/E_Commerce_Analytics) · [live](https://ecommerce-analytics-nexus.streamlit.app) | ETL + statistical inference + Apriori market basket analysis over 100K+ transactions |
| [human_activity_recognition](https://github.com/Parvptl/human_activity_recognition) | PCA-based feature reduction (561→102 dims) improving SVM accuracy from 93.6% to 96.17% |
| [Fintrack_Db](https://github.com/Parvptl/Fintrack_Db) | Full-stack portfolio manager — normalized PostgreSQL schema, ACID transactions, role-based access |

---

### Flagship — 4th Rank, Inter IIT Tech Meet 14.0

Algorithmic Optimisation Challenge, Genuity IO · competed against 20+ IIT teams

Built **TopoGAN**, integrating persistent homology-based losses into adversarial training for topology-preserving synthetic tabular data — outperforming StandardGAN, CTGAN, and TVAE. Paired it with a GPU-accelerated fusion pipeline (VAE, CatBoost, ensemble modeling) and a hierarchical semantic retrieval system using recursive K-Means with adaptive top-k routing.

`25–32%` statistical similarity improvement · `17–22%` downstream classification utility gain

[Repository](https://github.com/hemant030406/semantic_tree_based_document_retrieval)

---

### Where I've Worked Across the Stack

| Area | What I've built |
|---|---|
| **Production ML serving** | Containerized inference APIs with graceful degradation, health checks, and input validation |
| **Real-time systems** | Buffering pipelines decoupling high-frequency data ingestion from UI/render rate |
| **NLP** | Entity-aware sentiment models, transformer fine-tuning, leakage-safe temporal pipelines |
| **Computer vision & explainability** | Video deepfake detection with Grad-CAM-based interpretability |
| **Signal processing** | Bandpass filtering and peak detection for physiological waveform analysis |

---

### Technical Skills

| | |
|---|---|
| **Languages** | Python, Java, TypeScript/JavaScript, SQL, C++ |
| **Backend & APIs** | FastAPI, REST API design, Docker, Pydantic |
| **ML & Deep Learning** | PyTorch, Transformers, CNNs, Scikit-Learn, XGBoost, LightGBM |
| **Mobile** | React Native |
| **Foundations** | Data Structures & Algorithms, Operating Systems, Database Management |

---

Reach me at [parv4careers@gmail.com](mailto:parv4careers@gmail.com) or [LinkedIn](https://linkedin.com/in/parvptl).
