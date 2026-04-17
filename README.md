<div align="center">

# Gökdeniz Gülmez

**ML Researcher · Open-Source Engineer · Apple Silicon ML Ecosystem**

[![GitHub followers](https://img.shields.io/github/followers/Goekdeniz-Guelmez?style=flat&color=000&labelColor=111&logo=github)](https://github.com/Goekdeniz-Guelmez)
[![arXiv](https://img.shields.io/badge/arXiv-research-b31b1b?style=flat&logo=arxiv&logoColor=white)](https://arxiv.org/search/?searchtype=author&query=Gökdeniz+Gülmez)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-ea4aaa?style=flat&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/Goekdeniz-Guelmez)

*Stuttgart, Germany — building the infrastructure that makes local AI actually work.*

</div>

---

I build the tools that let researchers and engineers run, train, and understand large language models on their own hardware — specifically Apple Silicon. My work spans core MLX contributions, independent research published on arXiv, and open-source projects used by thousands.

If my work has saved you GPU bills, unlocked fine-tuning on your Mac, or ended up in your pipeline — consider [sponsoring](https://github.com/sponsors/Goekdeniz-Guelmez). Everything I build is free, maintained in my spare time, and driven by the belief that capable AI tooling shouldn't require a data center.

---

## Research
| Paper | Description | Year |
|---|---|---|
| [**JOSIEfied Qwen3.5 Gabliterated Models**](https://huggingface.co/collections/Goekdeniz-Guelmez/josiefied-qwen35-gabliterated) | Newest iteration of the JOSIEfied model family — now with vision support | 2026 |
| [**DynaMoE**](https://arxiv.org/abs/2603.01697) | Dynamic, adaptive Mixture-of-Experts LLM architecture | 2026 |
| [**JOSIE Models**](https://huggingface.co/collections/Goekdeniz-Guelmez/josie-11) | World's first fully fine-tuned model family trained entirely on Apple Silicon | 2026 |
| [**JOSIEfied Qwen3 Abliterated Models**](https://huggingface.co/collections/Goekdeniz-Guelmez/josiefied-and-abliterated-qwen3) | Reached **#1 globally** on uncensored benchmarks | 2025 |
| [**Gabliteration**](https://arxiv.org/abs/2412.06527) | Automated Gabliteration for any Transformers-compatible LLM | 2025 |
 
---

## Open-Source Projects

### 🔥 [mlx-lm-lora](https://github.com/Goekdeniz-Guelmez/mlx-lm-lora)
**Train large language models natively on Apple Silicon**

LoRA, QLoRA, and full-precision fine-tuning for LLMs — built on MLX. Supports Preference Optimization, RLHF, RL with and custom reward functions. The go-to fine-tuning toolkit for anyone running Apple Silicon.

- Full-precision, LoRA, and QLoRA training modes
- 12+ training methods and algorythms
- WandB integration for training metrics
- Multiple optimizer support including Muon
- [Example notebooks](https://github.com/Goekdeniz-Guelmez/mlx-lm-lora-example-notebooks)

---

### 🔬 [MLX-LM-LENS](https://github.com/Goekdeniz-Guelmez/mlx-lm-lens)
**Abliterate and research the inner workings of LLMs**

Interpretability and intervention tooling for language models in MLX. Understand what's happening inside your model, not just what comes out.

---

### 📚 [Local NotebookLM](https://github.com/Goekdeniz-Guelmez/Local-NotebookLM)
**Your own Google's NotebookLM — fully local, fully private**

PDF-grounded audio generation (podcasts, summaries, and many more with up to 6 speakers) running entirely on-device. No API keys, no cloud, no data leaving your machine. As well as a compation native App in [Local NotebookLM-App](https://github.com/Goekdeniz-Guelmez/Local-Notebook-LM-App).

---

### 🧪 [MLX-Embeddings-LoRA](https://github.com/Goekdeniz-Guelmez/mlx-embeddings-lora)
**Fine-tune embedding models natively on Apple Silicon**

Train and adapt embedding models for retrieval, search, and semantic tasks — directly in MLX.

---

### 📐 [MLX-Benchmark](https://github.com/Goekdeniz-Guelmez/MLX-Benchmark)
**Benchmark LLMs on Apple MLX framework knowledge and coding tasks.**

MLX Benchmark is the first comprehensive CLI tool and dataset that measures how well large language models understand, write, and debug code for Apple's MLX machine learning framework — covering everything from core array operations to LoRA fine-tuning with mlx-lm, mlx-vlm, and mlx-embeddings.

---

### 📐 [MLX-KAN](https://github.com/Goekdeniz-Guelmez/mlx-kan)
**Kolmogorov-Arnold Networks in MLX**

Native MLX implementation of KANs — a fundamentally different alternative to MLPs, implemented cleanly for Apple Silicon.

---

### 🧬 [Gabliteration](https://github.com/Goekdeniz-Guelmez/gabliteration)
**Automated abliteration for any Transformers LLM**

Companion code to [arXiv:2412.06527](https://arxiv.org/abs/2412.06527). Remove refusal directions from any model supported in Hugging Face Transformers.

---

### 🤖 [Josiefied Model Family](https://medium.com/@goekdeniz-guelmez/how-i-built-the-josiefied-models-e6050b8887a8)
A family of fine-tuned models that reached **#1 globally** on relevant benchmarks ([arXiv:2512.18901](https://arxiv.org/abs/2512.18901)).

---

## Contributions to the MLX Ecosystem

I'm an officially acknowledged contributor to the core MLX stack:

- [`ml-explore/mlx`](https://github.com/ml-explore/mlx/blob/main/ACKNOWLEDGMENTS.md) — core framework
- [`ml-explore/mlx-lm`](https://github.com/ml-explore/mlx-lm/blob/main/ACKNOWLEDGMENTS.md) — language model inference & training
- [`ml-explore/mlx-examples`](https://github.com/ml-explore/mlx-examples/blob/main/ACKNOWLEDGMENTS.md) — reference implementations
- [`Blaizzy/mlx-vlm`](https://github.com/Blaizzy/mlx-vlm) — vision-language models

### Architectures I've added to MLX / MLX-LM:

<details>
<summary>Expand full list</summary>

| Model | Organization |
|---|---|
| Mamba v1 & v2 | State Space |
| MiniCPM & MiniCPM3 | OpenBMB |
| Helium | Kyutai |
| GLM, GLM4, GLM5 | Z.ai & THUKEG |
| dots.llm1 | Rednote |
| Ernie4.5 MoE | Baidu |
| Bailing MoE & Bailing MoE Linear (Ling-family) | inclusionAI |
| Granite MoE | IBM |
| LongCat | Meituan |
| Nemotron H | NVIDIA |
| Apertus | Swiss-AI |
| OLMoE & OLMo 3 | AllenAI |
| Jamba | AI21 Labs |
| And many more... |  |

</details>

### Training features I've contributed:

- Full weight fine-tuning support in mlx-lm
- Muon optimizer (both mlx and mlx-lm)
- WandB metric reporting during training
- Multiple optimizer choices for training runs
- ReLU² activation function in core MLX

---

## Currently Building

### J.O.S.I.E.-Home
*A fully local, real-time, full-duplex multimodal assistant for smart home control*

A discrete diffusion language model with a custom tokenizer (ChatML-style format, hardcoded vocabulary covering rooms, devices, properties, and continuous value bins) that can autonomously control and manage a complete smart home environment — sensors, cameras, LEDs, and more. Fully offline. No cloud dependency.

Current focus: training data generation strategies and model architecture validation.

### Josie-Linear
A new Linear Dynamic Mixture-of-Experts LLM architecture — currently in development.

---

## Support This Work

Everything above — the MLX contributions, the research, the open-source tools — is built in my spare time. If any of it has been useful to you or your team, [sponsoring](https://github.com/sponsors/Goekdeniz-Guelmez) directly funds continued development, faster bug fixes, and new features.

[![Sponsor Gökdeniz](https://img.shields.io/badge/Sponsor%20on%20GitHub-%E2%9D%A4%EF%B8%8F-ea4aaa?style=for-the-badge&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/Goekdeniz-Guelmez)

---

## GitHub Activity

<p align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=Goekdeniz-Guelmez&theme=github-compact" alt="GitHub activity graph"/>
</p>

---

<div align="center">
<sub>Stuttgart, Germany · ML Researcher & Engineer · Apple Silicon AI Tooling</sub>
</div>
