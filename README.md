# ⚡ LENS: Lightweight and Explainable LLM-Based APT Detection at the Edge for 6G Security

This repository contains the **source code**, **experimental setup**, and **modified baseline implementations** for the paper:

📄 **“LENS: Lightweight and Explainable LLM-Based APT Detection at the Edge for 6G Security”**  
*(Published in IEEE Access, 2025)*

---

## 📁 Repository Structure

- **`LENS.ipynb`** → Main notebook containing the core experimental workflow.  
- **`deeplog_modified/`, `earlycrow_modified/`** → Enhanced baseline implementations of DeepLog and EarlyCrow.  
- **`notes/`** → Translated experiment notes (originally in Turkish).  
- **`onnx_models/`** → ONNX-exported versions of trained models for edge deployment.  

---

## 🧪 Experiment Overview

Experiments were conducted on three dataset subsets (**5 %**, **30 %**, and **100 %**) to evaluate scalability and generalization.

- **Objective:** Detect Advanced Persistent Threats (APTs) in **Industrial IoT (IIoT)** systems.  
- **Scope:** Designed for **6G edge-centric cybersecurity** architectures.  
- **Metrics:** Accuracy, F1-score, latency, energy consumption, and resource utilization.

---

## 🌐 Dataset — CICAPT-IIOT 2024

All experiments are based on the **CICAPT-IIOT 2024** dataset, a provenance-based APT dataset for IIoT environments.

**Reference:**  
> Ghiasvand, E., et al.  
> *“CICAPT-IIOT: A provenance-based APT attack dataset for IIoT environment.”*  
> arXiv preprint [arXiv:2407.11278](https://arxiv.org/abs/2407.11278) (2024)

🔗 The dataset is publicly available online (search for **“CICAPT-IIOT 2024”**).

---

## ⚙️ Edge & Cloud Deployment

### 🖥️ Edge Platform
Evaluated on a **Raspberry Pi 4**, demonstrating lightweight APT detection feasibility on constrained edge devices.

### ☁️ Cloud Runtime
The **LLM components** were executed on [Lightning.ai](https://lightning.ai/), which offers **15 hours of free compute** for rapid prototyping.

---

## 🧠 ONNX Format & Raspberry Pi Compatibility

To enable low-power inference, trained models are also exported to **ONNX** format.

**Directory:** `onnx_models/`  
Includes:
- ONNX-exported model files  
- Example inference script: `inference_rpi.py`

**Benefits of ONNX Deployment**
- Optimized for **ARM-based edge devices** (e.g., Raspberry Pi 4)  
- Compatible with **ONNX Runtime**, **TensorRT**, **OpenVINO**  
- Enables **real-time APT detection** with minimal resources

---

## 🔧 Baseline Enhancements

Enhanced baselines adapted for 6G edge cybersecurity:
- **DeepLog**  
- **EarlyCrow (EarlyBird)**  

**Improvements:**
- Dataset preprocessing optimization  
- Hyperparameter tuning for IIoT log data  
- Compatibility with PyTorch ≥ 2.0 and ONNX export  
- Performance + explainability alignment with LENS pipeline

---

## 🚀 How to Run

Install required dependencies (a `requirements.txt` file may be added later):

```bash
# Run the main experiment (30% subset)
python subset30_original.py


## 📖 To Cite

If you use this repository or refer to its results, please cite:

> **S. B. Melhem, M. Göleç, A. Alwarafy, and Y. Khamayseh**,  
> “LENS: Lightweight and Explainable LLM-Based APT Detection at the Edge for 6G Security,”  
> *IEEE Access*, 2025.

```bibtex
@article{melhem2025lens,
  title     = {LENS: Lightweight and Explainable LLM-Based APT Detection at the Edge for 6G Security},
  author    = {Melhem, Suhib Bani and Golec, Muhammed and Alwarafy, Abdulmalik and Khamayseh, Yaser},
  journal   = {IEEE Access},
  year      = {2025},
  publisher = {IEEE}
}
