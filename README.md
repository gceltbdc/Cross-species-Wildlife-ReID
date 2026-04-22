# 🐯🐄 Frequency-Aware Vision Transformer for Cross-Species Animal Re-Identification

> **A unified deep learning framework for identifying individual animals across species using high-frequency visual cues.**  
> Designed and evaluated on **Amur Tigers** and **Holstein-Friesian Cows**.

---

## 🌍 Overview

Animal Re-Identification (ReID) aims to recognize the same individual animal across different images, cameras, time periods, or environments.

Unlike generic classification, ReID must distinguish **individual identities** within the same species.

This project introduces a **Frequency-Aware Vision Transformer (FA-ViT)** that learns highly discriminative identity features such as:

- 🐯 Tiger stripe topology  
- 🐄 Cow coat patch distributions  
- Fur textures & contour boundaries  
- Shape-consistent local patterns  
- High-frequency biometric signals

---

## ✨ Why This Project Matters

### Wildlife Conservation
- Track endangered tigers in the wild
- Reduce manual camera-trap labeling
- Improve population monitoring

### Smart Livestock Farming
- Identify individual cows automatically
- Monitor movement, health, and productivity
- Replace RFID/manual tagging systems

---

# 🚀 Key Contributions

✅ Unified ReID framework for **wildlife + livestock**

✅ Supports two visually different species:
- **Amur Tiger**
- **Holstein-Friesian Cow**

✅ Introduces frequency-domain identity learning

✅ Adds complete **CMC curve analysis**

✅ Achieves:

| Dataset | Rank-1 | Rank-5 | mAP |
|--------|--------|--------|------|
| ATRW Tiger | **92.31%** | **98.52%** | **92.84%** |
| MultiCamCows2024 | **96.43%** | **100.0%** | **96.50%** |

---

# 🧠 Model Architecture

The framework combines three major modules:

## (a) Frequency-Domain Mixed Augmentation (FMA)

Transforms images into frequency space using FFT and learns stable identity patterns.

Improves robustness against:

- Illumination changes
- Pose variation
- Blur
- Background clutter

---

## (b) Object-Aware Dynamic Selection (ODS)

Uses transformer attention maps to retain only identity-relevant tokens.

Examples:

- Tiger stripe zones
- Cow patch boundaries

---

## (c) Feature Equilibrium Loss (FEL)

Balances:

- RGB visual features
- High-frequency texture features

Prevents overfitting to noisy frequency details.

---

# 📊 Datasets Used

## 🐯 ATRW Dataset (Amur Tiger)

- 92 identities
- Real-world wild tiger images
- Pose + occlusion + forest clutter

## 🐄 MultiCamCows2024 Dataset

- 46 Holstein-Friesian cows
- Multi-camera farm environment
- Side-view and motion variations

---

# 📈 Evaluation Metrics

We report:

- Rank-1 Accuracy
- Rank-5 Accuracy
- mAP
- mINP
- CMC Curves

---

# 🖼 Sample Identity Traits Learned

## Tiger
- Stripe continuity
- Face side-patterns
- Fur boundaries

## Cow
- Black-white patch geometry
- Neck/torso spot shapes
- Side coat distribution

---
# 📉 CMC Curve Example

```text
Tiger:
Rank-1  ██████████████ 92.31%
Rank-5  ███████████████████ 98.52%

Cow:
Rank-1  ████████████████ 96.43%
Rank-5  ████████████████████ 100%
```

---

# 🔬 Research Impact

This work demonstrates that **frequency-domain biometrics** are transferable across species.

Meaning:

> stripes, textures, boundaries, and coat topology can become universal identity signals.





