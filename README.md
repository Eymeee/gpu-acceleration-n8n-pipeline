# GPU Speedup + Profiling (3 Notebooks) + n8n Integration

This repo is a team project with two parts:

## 1) GPU Acceleration & Profiling (80%)
We build **3 small ML projects** and compare **CPU vs GPU** runtime.
Each project is implemented in a **Jupyter notebook** and includes:
- CPU baseline timing
- GPU timing (CUDA)
- **Speedup = CPU time / GPU time**
- Profiling (to explain why it speeds up or slows down)

Notebooks:
- `notebooks/p1_gpu_acceleration.ipynb`
- `notebooks/p2_gpu_acceleration.ipynb`
- `notebooks/p3_gpu_acceleration.ipynb`

## 2) Real-World Integration with n8n (20%)
We implement an **n8n workflow**:
User enters a **book/article title** → web search → scraping (Firecrawl) → parsing →  
**key ideas + long summary (~10 pages) + text-to-speech (TTS)**.

n8n exports:
- `integration/n8n/workflows/`

## Quick Start
```bash
python -m venv .venv
source .venv/bin/activate   
pip install -r requirements.txt
jupyter lab
```

## Repo structure
```bash
notebooks/        # results inside the notebooks
src/common/       # shared utilities (timing, device, helpers)
integration/n8n/  # n8n workflow exports (JSON)
data/             # optional datasets
```
