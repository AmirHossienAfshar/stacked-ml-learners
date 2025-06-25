# Stacked ML Learners

This project is part of the *Computational Intelligence* course at Ferdowsi University of Mashhad. It explores a two-phase approach to improving classification performance using CNN-based feature extraction and stacked ensemble learning.

---

### Dataset

The dataset includes images from **three categories**:
- Horses  
- Cats  
- Dogs  

The same dataset is used throughout all phases of the project.

---

### Phase 1: Feature Extraction & Classification

- Used **ResNet-18** as a feature extractor.
- Extracted feature vectors from three levels of the network:
  - **Initial features**: Layers up to `maxpool` (e.g., `conv1`, `bn1`, `relu`)
  - **Mid-level features**: Layers up to `block2`
  - **High-level features**: Full network up to `avgpool` (excluding FC)
- Trained **at least 4 classifiers** on these feature vectors.
- Evaluated and compared the performance of classifiers based on different feature levels.

---

### Phase 2: Stacked Learners

- Implemented a custom **stacked ensemble model** using at least 4 classifiers.
- Performed **hyperparameter tuning** for each base classifier.
- Combined classifiers manually to form the final stacked learner (no built-in stackers used).
- Actively monitored and prevented **overfitting** using class materials.
  - If none of the base models overfitted, one intentionally overfitted model was included for correction.
- Final stacked model was evaluated and **compared to Phase 1 results**.

---

### Input to the Stacker

- The stacker receives **feature vectors** from Phase 1 as inputs.
- Feature vectors from each class (horse, cat, dog) were used independently and then merged.

---

### Evaluation & Reporting

- All phases were evaluated using standard metrics (accuracy, precision, etc.).
- Result graphs and detailed analysis are included in the `docs/` folder.
- The **Persian-language documentation** explaining all implementation details is included.

---
