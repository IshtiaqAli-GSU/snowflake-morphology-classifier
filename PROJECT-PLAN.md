# ❄️ Final Project Plan  
**CSC/DSCI 4851/6851 — Fall 2025**  
**Team Members:** Ishtiaq Chowdhury & Ali [Last Name]  
**Project Title:** *Snowflake Morphology Classification Using Deep Learning*  

---

## 📅 Important Dates

| Milestone | Deliverable | Due Date | Status |
|------------|--------------|----------|---------|
| Project Proposal | 1-paragraph proposal (PDF) | ✅ Oct 10 2025 | **Submitted** |
| Project Milestone | 2–3 page report + presentation | ⏳ Oct 31 2025 | **In progress** |
| Final Report & Presentation | 6–8 page CVPR-style paper + slides | ⏳ Dec 12 2025 | **Upcoming** |

---

## 🧭 Project Overview
We are developing a **deep learning classifier** to categorize snowflake morphologies into five types—**dendrites, plates, columns, aggregates, and graupel**—using the **MASCDB (Multi-Angle Snowflake Camera Database)**.  
This is an *application-track* project applying **EfficientNet-B0** transfer learning to a scientific dataset for accurate yet computationally efficient classification.

---

## ⚙️ Step-by-Step Plan

### 🟢 **Phase 1 — Setup & Planning (Weeks 1–2)**
**Progress**
- [x] Project proposal written and approved  
- [x] GitHub repo initialized (`snowflake-morphology-classifier`) with Python `.gitignore`, MIT License, and README  
- [x] Decided to use **TensorFlow / Keras** (EfficientNet-B0 pretrained on ImageNet)  
- [X] Set up and verified Colab environment with GPU + Drive mount  
- [x] Created partial folder structure (adding others as needed)  

**Outputs**
- [x] `proposal.pdf`  
- [x] Repository initialized and organized for upcoming code/data  

---

### 📂 **Phase 2 — Data Collection & Preparation (Weeks 3–4)**
**Goals**
- [ ] Download a manageable **subset of MASCDB** from Zenodo (~20 k–50 k images)  
- [ ] Extract **metadata CSV** and keep only five classes (*Dendrites, Plates, Columns, Aggregates, Graupel*)  
- [ ] Reorganize into **folder-per-class** structure or maintain CSV label mapping  
- [ ] Split dataset into **train (70 %)**, **validation (15 %)**, and **test (15 %)**  
- [ ] Apply **data augmentation** (flip, rotate, brightness, contrast)  

**Outputs**
- [ ] Cleaned dataset folder (or CSV)  
- [ ] Preprocessing notebook (`data_prep.ipynb` or `data_prep.py`)  

---

### 🎤 **Phase 2.5 — Milestone Presentation (Week 5 → Due Oct 31)**
**Goals**
- [ ] Prepare and present slides summarizing Phases 1–2 and previewing Phase 3  

**Slide Components**
- **Background:** motivation, challenge, and scientific impact  
- **Problem Statement:** five-class snowflake classification objective  
- **Related Work:** Hicks et al. (2019), Key et al. (2021)  
- **Proposed Method:** EfficientNet-B0 architecture and training plan  
- **Data & Experiment:** MASCDB subset summary + sample visuals  
- **Next Steps:** training schedule and evaluation strategy  

**Outputs**
- [ ] `milestone_presentation.pptx` or `.pdf`  
- [ ] In-class presentation (Oct 31 2025)  

---

### 🧠 **Phase 3 — Model Development (Nov 1 – Nov 17)**
**Goals**
- [ ] Load **EfficientNet-B0 (pretrained on ImageNet)**  
- [ ] Replace top layer with 5-class softmax  
- [ ] Train in two stages:  
  1. Freeze backbone → train classification head  
  2. Unfreeze and fine-tune with low learning rate  
- [ ] Track training and validation accuracy/loss  

**Outputs**
- [ ] `train_model.ipynb`  
- [ ] Trained weights (`efficientnet_snowflake.h5`)  
- [ ] Accuracy/loss plots  

---

### 📊 **Phase 4 — Evaluation & Analysis (Nov 18 – Dec 1)**
**Goals**
- [ ] Evaluate model on test set  
- [ ] Generate confusion matrix + sample predictions  
- [ ] Compute Accuracy, Precision, Recall, and F1-score  
- [ ] (Optional) Visualize feature importance with Grad-CAM  

**Outputs**
- [ ] Evaluation notebook (`evaluate_model.ipynb`)  
- [ ] Figures folder (`figures/`)  

---

### 📝 **Phase 5 — Reporting & Final Delivery (Dec 2 – Dec 12)**
**Goals**
- [ ] Write 6–8 page **CVPR-style report** following rubric: Abstract, Intro, Related Work, Data, Methods, Experiments, Conclusion  
- [ ] Prepare **final presentation** including Analysis, Discussion, Extensions, and Conclusion  
- [ ] Package code and figures for supplementary submission  

**Outputs**
- [ ] `final_report.pdf`  
- [ ] `final_presentation.pptx` or `.pdf`  
- [ ] `supplementary.zip` (code + figures + optional demo video)  

---

## 🎯 Final Deliverable
A complete, reproducible **deep-learning pipeline** that:
- Takes **MASCDB snowflake images** as input  
- Predicts one of five morphology types (*Dendrite, Plate, Column, Aggregate, Graupel*)  
- Achieves ≈ 85–90 % accuracy via EfficientNet-B0 fine-tuning  
- Provides:  
  - Trained model + code  
  - Evaluation metrics and confusion matrix  
  - Visualization of predictions  
  - Final CVPR-format report and presentations
