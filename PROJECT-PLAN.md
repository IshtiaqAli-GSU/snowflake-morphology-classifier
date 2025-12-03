# ❄️ Final Project Plan  
**CSC/DSCI 4851/6851 — Fall 2025**  
**Team Members:** Ishtiaq Chowdhury & Ali Al Anbari  
**Project Title:** *Snowflake Morphology Classification Using Deep Learning*  

---

## 📅 Important Dates

| Milestone | Deliverable | Due Date | Status |
|----------|-------------|----------|--------|
| Project Proposal | 1-paragraph proposal (PDF) | ✅ Oct 10 2025 | **Submitted** |
| Project Milestone | 2–3 page report + presentation | ✅ Oct 31 2025 | **Completed & Presented** |
| Final Report & Presentation | 6–8 page CVPR-style paper + slides | ⏳ Dec 12 2025 | **Upcoming** |

---

## 🧭 Project Overview
We are developing a **deep learning classifier** to categorize snowflake morphologies into four types:  
**graupel, aggregate, planar_crystal**, and **columnar_crystal**, using the **MASCDB (Multi-Angle Snowflake Camera Database)**.

This is an *application-track* project using **EfficientNet-B0** transfer learning to build a lightweight model capable of classifying new, unlabeled snowflake images.

---

## ⚙️ Step-by-Step Plan

### 🟢 **Phase 1 — Setup & Planning (Weeks 1–2)**
**Progress**
- [x] Project proposal written and approved  
- [x] GitHub repo initialized  
- [x] Chose TensorFlow/Keras + EfficientNet-B0  
- [x] Set up and verified Google Colab GPU environment  
- [x] Created folder structure (repo + Drive)  

**Outputs**
- [x] `proposal.pdf`  
- [x] Repository prepared for development  

---

### 📂 **Phase 2 — Data Collection & Preparation (Weeks 3–4)**
**Progress**
- [x] Downloaded MASCDB dataset (`MASCdb.zarr.zip` and `MASCdb_triplet.parquet`)  
- [x] Extracted metadata and inspected available class labels  
- [x] Filtered dataset to four snowflake classes: **graupel, aggregate, planar_crystal, columnar_crystal**  
- [x] Saved filtered metadata to `filtered_labels.csv`  
- [x] Generated class counts and distribution plots  
- [x] Completed milestone slides and milestone report  

**Remaining Goals**
- [ ] Split dataset into **train (70%)**, **validation (15%)**, and **test (15%)**  
- [ ] Implement **data augmentation** to balance planar_crystal and columnar_crystal classes  

**Outputs**
- [x] Cleaned metadata file  
- [x] Class distribution figure (used in milestone)  
- [x] Milestone data-prep notebook  

---

### 🎤 **Phase 2.5 — Milestone Presentation (Week 5 → Due Oct 31)**
**Progress**
- [x] Created milestone slides  
- [x] Presented in class  
- [x] Submitted milestone report (2–3 pages)

**Outputs**
- [x] `milestone_presentation.pptx` / `.pdf`  
- [x] `milestone_report.pdf`  

---

### 🧠 **Phase 3 — Model Development (Nov 1 – Nov 17)**
**Goals**
- [ ] Load EfficientNet-B0 pretrained on ImageNet  
- [ ] Replace classification head with 4-class output  
- [ ] Build data pipeline with augmentation  
- [ ] Stage 1: Train classification head with backbone frozen  
- [ ] Stage 2: Fine-tune entire model with smaller learning rate  
- [ ] Test optimizers: Adam, RMSprop, SGD  
- [ ] Test regularization: dropout, L2, batch norm  
- [ ] Track training/validation accuracy and loss  

**Outputs**
- [ ] `train_model.ipynb`  
- [ ] Trained weights (`efficientnet_snowflake.h5`)  
- [ ] Loss/accuracy plots  

---

### 📊 **Phase 4 — Evaluation & Analysis (Nov 18 – Dec 1)**
**Goals**
- [ ] Evaluate model on test set  
- [ ] Generate confusion matrix  
- [ ] Report accuracy, precision, recall, F1-score  
- [ ] Visualize sample predictions  
- [ ] (Optional) Run Grad-CAM  

**Outputs**
- [ ] `evaluate_model.ipynb`  
- [ ] Figures folder (`figures/`)  

---

### 📝 **Phase 5 — Reporting & Final Delivery (Dec 2 – Dec 12)**
**Goals**
- [ ] Write final 6–8 page CVPR-style report  
- [ ] Create final presentation  
- [ ] Package code + figures + model for submission  

**Outputs**
- [ ] `final_report.pdf`  
- [ ] `final_presentation.pptx` / `.pdf`  
- [ ] `supplementary.zip`  

---

## 🎯 Final Deliverable
A complete, reproducible **deep-learning pipeline** that:
- Inputs MASCDB snowflake images  
- Predicts one of four snowflake morphology types  
- Achieves strong performance with modest compute resources  
- Includes:  
  - Trained EfficientNet-B0 model  
  - Evaluation metrics and confusion matrix  
  - Visualization of predictions  
  - Final CVPR-style report and presentation  
