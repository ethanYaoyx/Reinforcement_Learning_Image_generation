# 🧠 Reinforcement Learning Guided Medical Image Generation

This project leverages **Reinforcement Learning (RL)** to enhance **Stable Diffusion** for generating high-quality synthetic medical images. It includes two training stages:

- **Stage 1**: Trains a selector model to evaluate image quality.
- **Stage 2**: Uses the selector to guide the Stable Diffusion model to generate better-quality images based on feedback.

## 📁 Project Features

- ✅ Prompt-based medical image generation (e.g., "Chest X-Ray", "OCT", etc.)
- ✅ Selector model based on ViT to assess image quality.
- ✅ Reinforcement feedback loop improves generation quality across stages.
- ✅ Full pipeline implemented in PyTorch and HuggingFace.

## 🧪 Result (FID Scores)

| Model              | FID     |
|-------------------|---------|
| Stable Diffusion  | 306.988 |
| Stage 1           | 243.730 |
| Stage 2           | 132.863 |

## 📦 Generated Images

👉 [Download generated images here](https://yuad-my.sharepoint.com/:f:/g/personal/yyao3_mail_yu_edu/EnKagxzbu3hEnHSieVPjNhABc-4tBf-rtDFMhc2CQ_f5xw?e=CXYuVh)

## ⚙️ Config Overview

You can find all model, selector, and generation settings in `config.yaml`.

- Models used:
  - ViT + CLIP for policy and selector models
  - Stable Diffusion for image synthesis
- Training consists of two stages with adjustable thresholds and augmentation
- Data is prompted using CSV files with modality descriptions

---

Feel free to clone and customize the pipeline for your medical image generation tasks.
