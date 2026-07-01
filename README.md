<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0a0b,100:0a0a0b&height=180&section=header&text=Parv%20Patel&fontSize=52&fontColor=e8e6e1&fontAlignY=42&desc=ML%20%26%20Backend%20Engineer%20%C2%B7%20IIT%20Palakkad&descSize=16&descAlignY=62&descColor=8b8a86&animation=fadeIn" width="100%"/>

<br/>

<a href="https://parvpatel.me"><img src="https://img.shields.io/badge/portfolio-parvpatel.me-c17a3f?style=flat-square&labelColor=0a0a0b" /></a>
<a href="https://linkedin.com/in/parvptl"><img src="https://img.shields.io/badge/linkedin-parvptl-c17a3f?style=flat-square&labelColor=0a0a0b" /></a>
<a href="mailto:parv4careers@gmail.com"><img src="https://img.shields.io/badge/email-parv4careers-c17a3f?style=flat-square&labelColor=0a0a0b" /></a>
<a href="https://github.com/Parvptl"><img src="https://img.shields.io/badge/status-shipping-5a9b76?style=flat-square&labelColor=0a0a0b" /></a>

</div>

<br/>

```
I build machine learning systems as production services, not notebooks.
Most of the work is at the boundary between a trained model and the API
that has to serve it reliably — validation, graceful failure, concurrency,
the parts that don't show up in an accuracy number.
```

Currently: explainable AI for enterprise IAM at Accenture, and the backend
for a clinician vitals platform at IIT Palakkad.

<br/>

## Selected Work

<table>
<tr>
<td width="100%">

### [DualForensics](https://github.com/Prish1509/Deep-Fake-Detection) — Deepfake Detection Service
[![Live](https://img.shields.io/badge/live_demo-deepfake.parvpatel.me-0a0a0b?style=flat-square&labelColor=c17a3f)](https://deepfake.parvpatel.me)

A CNN-Transformer video classifier served through a containerized FastAPI microservice. The engineering problem wasn't the model — it was making it survive bad input and concurrent load.

```
upload → validate → preprocess → infer → explain → respond
```

- Model loading decoupled from service lifecycle via a dedicated `/api/health` check — a corrupted checkpoint returns a clean `503`, not a crash
- Payload validation at the edge, exception-safe temp-file cleanup, single-threaded OMP/MKL tuning to stop concurrent requests contending for CPU cores
- `0.9787` AUC on FaceForensics++ · Grad-CAM explainability compiled into one optimized response payload

`Python` `PyTorch` `FastAPI` `Docker` `OpenCV`

</td>
</tr>
<tr>
<td width="100%">

### [Hesor](https://github.com/Akshat-42/Hesor) — Real-Time Vitals Dashboard

A React Native app rendering high-frequency physiological waveforms without stuttering the UI.

```
stream → buffer(ref) → flush@10Hz → DSP → classify → render@60fps
```

- Samples buffer into a mutable ref, not React state — a single interval flushes and downsamples into state at 10Hz, decoupling ingestion rate from render rate
- Signal processing (bandpass filtering, AMDF peak detection) written as pure, unit-testable functions
- FastAPI backend handles blood-pressure classification from 5-second signal blocks with strict Pydantic validation

`React Native` `TypeScript` `FastAPI` `Scikit-Learn`

</td>
</tr>
<tr>
<td width="100%">

### [Financial Sentiment Forecasting](https://github.com/Parvptl/Financial_Sentiment_Forecasting) — Entity-Aware Transformer Pipeline

An end-to-end pipeline over 25K+ entity-level financial news instances.

```
ingest → encode(DeBERTa) → extract features → window(leakage-safe) → model ×6 → validate
```

- DeBERTa-v3 fine-tuned for aspect-based sentiment (`92%+` accuracy); outputs decoupled as reusable features so 6+ downstream models train without retraining the transformer
- Return labels use causally shifted rolling windows across 1/2/5-day horizons — no lookahead leakage
- Validated with ablation studies and 2,000-sample bootstrap significance testing

`Python` `PyTorch` `Transformers` `XGBoost` `LightGBM`

</td>
</tr>
</table>

<br/>

## Other Public Repositories

<details>
<summary><b>4 more repositories — click to expand</b></summary>
<br/>

| Repository | What it is |
|---|---|
| [maxflow_visualizer](https://github.com/Parvptl/maxflow_visualizer) · [live](https://flow.parvpatel.me) | Ford-Fulkerson, Edmonds-Karp, and Push-Relabel implemented from scratch, with a D3.js engine animating the Max-Flow Min-Cut theorem |
| [E_Commerce_Analytics](https://github.com/Parvptl/E_Commerce_Analytics) · [live](https://ecommerce-analytics-nexus.streamlit.app) | ETL + statistical inference + Apriori market basket analysis over 100K+ transactions |
| [human_activity_recognition](https://github.com/Parvptl/human_activity_recognition) | PCA-based feature reduction (561→102 dims) improving SVM accuracy from 93.6% to 96.17% |
| [Fintrack_Db](https://github.com/Parvptl/Fintrack_Db) | Full-stack portfolio manager — normalized PostgreSQL schema, ACID transactions, role-based access |

</details>

<br/>

## Flagship — 4th Rank, Inter IIT Tech Meet 14.0

<img src="https://img.shields.io/badge/rank-4th%20of%2020+%20IIT%20teams-c17a3f?style=flat-square&labelColor=0a0a0b" />
<img src="https://img.shields.io/badge/challenge-algorithmic%20optimisation-8b8a86?style=flat-square&labelColor=0a0a0b" />
<img src="https://img.shields.io/badge/host-genuity%20io-8b8a86?style=flat-square&labelColor=0a0a0b" />

Built **TopoGAN**, integrating persistent homology-based losses into adversarial training for topology-preserving synthetic tabular data — outperforming StandardGAN, CTGAN, and TVAE. Paired it with a GPU-accelerated fusion pipeline (VAE, CatBoost, ensemble modeling) and a hierarchical semantic retrieval system using recursive K-Means with adaptive top-k routing.

| Metric | Result |
|---|---|
| Statistical similarity | `+25–32%` over baseline generative models |
| Downstream classification utility | `+17–22%` |
| Baselines outperformed | StandardGAN, CTGAN, TVAE |

[→ Repository](https://github.com/hemant030406/semantic_tree_based_document_retrieval)

<br/>

## Where I've Worked Across the Stack

| Area | What I've built |
|---|---|
| 🔧 **Production ML serving** | Containerized inference APIs with graceful degradation, health checks, input validation |
| ⚡ **Real-time systems** | Buffering pipelines decoupling high-frequency data ingestion from UI/render rate |
| 🧠 **NLP** | Entity-aware sentiment models, transformer fine-tuning, leakage-safe temporal pipelines |
| 👁 **Computer vision & explainability** | Video deepfake detection with Grad-CAM-based interpretability |
| 📡 **Signal processing** | Bandpass filtering and peak detection for physiological waveform analysis |

<br/>

## Technical Skills

<table>
<tr><td valign="top" width="50%">

**Languages**
`Python` `Java` `TypeScript` `JavaScript` `SQL` `C++`

**Backend & APIs**
`FastAPI` `REST API Design` `Docker` `Pydantic`

</td><td valign="top" width="50%">

**ML & Deep Learning**
`PyTorch` `Transformers` `CNNs` `Scikit-Learn` `XGBoost` `LightGBM`

**Mobile**
`React Native`

</td></tr>
</table>

<br/>

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Parvptl&show_icons=true&hide_border=true&bg_color=0a0a0b&title_color=e8e6e1&text_color=8b8a86&icon_color=c17a3f&hide=prs" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Parvptl&layout=compact&hide_border=true&bg_color=0a0a0b&title_color=e8e6e1&text_color=8b8a86&langs_count=6" height="165"/>

</div>

<br/>

<div align="center">

[parv4careers@gmail.com](mailto:parv4careers@gmail.com) · [LinkedIn](https://linkedin.com/in/parvptl) · [parvpatel.me](https://parvpatel.me)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0a0b,100:0a0a0b&height=60&section=footer"/>

</div>
