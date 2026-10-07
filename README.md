# Hi, I'm Om 👋

MS Computer Science (AI) student at **USC** (expected May 2027), working on **ML systems and infrastructure**: running, evaluating, and debugging models end to end.

Based in Los Angeles, CA.

---

## What I'm working on

- 🔬 **Research Volunteer, [GLAMOR Lab](https://glamor-usc.github.io/) (USC)**: robustness evaluation of Vision-Language-Action (VLA) models for robotic manipulation, advised by Prof. Jesse Thomason.
- 🧠 **LLM council routing**: a learned router that decomposes tasks and assigns them to the right model (team project, details below).
- ⚙️ **Sharpening C++ and data structures & algorithms** for systems-oriented roles.

---

## Projects

### [Task-Aware Orchestration for LLM Councils](https://github.com/Task-Aware-LLM-Council/Task-Aware-LLM-Council)
USC CSCI-544 (NLP) · team of 5 · Spring 2026

- Owned the **council-policy** and **training** packages.
- Built the **learned router** end to end: a Gemma-LoRA seq2seq decomposer-router with atomicity-constrained force-routing for math and code, covering dataset construction, training, featurization, and routing policy.
- Diagnosed a multi-hop QA (MuSiQue) failure by bucketing errors into abstention, extraction, and model-wrong modes. Fixes (oracle-context injection, scratchpad prompting, abstention-aware scoring) raised token-F1 from **<0.17 to ~0.65**.
- Ran evaluations on USC CARC (SLURM, A40 GPUs, vLLM + Apptainer) across MuSiQue, QuALITY, FEVER, HARDMath, and HumanEval+.

*Teammates built the model gateway and benchmark runner; I built the routing and policy layers.*

### [Fingerprint Matching with a Siamese Network](https://github.com/OmGhag/FingerPrintMatchingSNN)
- Shared-weight CNN Siamese network trained on ~38K augmented pairs from the SOCOFing dataset, using binary cross-entropy loss.
- Ran a **merge-strategy ablation**: element-wise subtraction reached **97.7%** validation accuracy, while an L1-distance merge stayed near chance (~57%).
- Exported to TFLite and profiled latency.

### Multimodal Plant Disease Detection
- Four-input fusion model: MobileNetV2 image branch, dual-window LSTM temporal subnets, and a dense tabular branch (608-dim fused representation) over 38 classes and 14 species (PlantVillage, 54K+ images).
- Served through a Flask REST API with a JS frontend, at sub-200 ms inference.
- Found and fixed a silent train/inference preprocessing mismatch.
- **Documented a label-leakage issue**: the synthetic soil and weather features were generated per class, so they encode the label. The README explains why the multimodal accuracy isn't a valid measure of fusion benefit.

---

## Tech

**Languages:** Python · C++ (in progress)
**ML / DL:** PyTorch · JAX · TensorFlow / TFLite · LoRA fine-tuning
**Systems:** vLLM · SLURM · Apptainer · Flask · REST APIs
**Research tooling:** LIBERO benchmark · VLA models (OpenVLA, π0, π0-FAST)

---

## Education

- **M.S. Computer Science (AI)**, University of Southern California · GPA 3.70 · expected May 2027
- **B.E. Computer Engineering (AI)**, Vidyalankar Institute of Technology, Mumbai · 2021 – 2025

---

## Get in touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Om%20Ghag-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/om-ghag-41745314a/)
[![Email](https://img.shields.io/badge/Email-omghag2003%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:omghag2003@gmail.com)
