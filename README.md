# 🧬 Breast Histopathology Image Classification using CNNs & Transfer Learning  

## 📌 Project Overview  
This project focuses on building an AI model for detecting breast cancer from histopathology images. The dataset consists of thousands of patient biopsy image patches that are split into two categories: **cancerous** and **non-cancerous**.  

Our objective was to apply **Deep Learning techniques (CNNs & Transfer Learning)** to extract meaningful features from the images and build robust models capable of accurately classifying them.  

---

## 📂 Dataset  
- **Source:** [IDC_regular_ps50_idx5.zip](http://gleason.case.edu/webdata/jpi-dl-tutorial/IDC_regular_ps50_idx5.zip)  
- **Acknowledgements:**  
  - [NIH PubMed Paper](https://www.ncbi.nlm.nih.gov/pubmed/27563488)  
  - [SPIE Conference Paper](http://spie.org/Publications/Proceedings/Paper/10.1117/12.2043872)  

The dataset contains histopathology image patches of breast cancer, labeled as **cancer** or **not cancer**.  

---

## 🛠️ Major Libraries Used  
- **TensorFlow/Keras** → Model creation, training, and data augmentation  
- **Matplotlib** → Visualization of results (accuracy/loss graphs, confusion matrices)  

---

## 🔑 Steps Followed  

1. **Data Preparation**  
   - Selected ~250 patients from the dataset.  
   - Split into two folders: `cancer` and `not_cancer`.  

2. **Data Augmentation**  
   - Applied synthetic variations using **ImageDataGenerator** (rotation, flipping, zoom, etc.).  
   - Helped enrich the dataset and improve generalization.  

3. **Train-Test Split**  
   - Created separate training and testing datasets for evaluation.  

4. **Model Development**  
   Implemented and compared multiple models using **Transfer Learning** and training from scratch:  
   - ✅ VGG16 (Imagenet weights, frozen base layers)  
   - ✅ VGG16 (Imagenet weights, unfreezing top 4 base layers)  
   - ✅ EfficientNetB0 (all layers trainable from scratch)  
   - ✅ EfficientNetB3 (all layers trainable from scratch)  
   - ✅ VGG16 (Imagenet weights, partial unfreezing of multiple layers)  
   - ✅ VGG16 (Imagenet weights, all layers unfrozen, full retraining)  

5. **Training Techniques**  
   - Used **EarlyStopping** to prevent overfitting.  
   - Applied **ReduceLROnPlateau** for adaptive learning rate scheduling.  

6. **Evaluation**  
   - Plotted **accuracy and loss curves** (training vs validation).  
   - Visualized **confusion matrices** to assess classification performance.  

---

## 📊 Results  

👉 *(Replace with your actual results once ready)*  

- **Best Model:** VGG16 with Imagenet weights + partially unfrozen layers  
- **Validation Accuracy:** ~XX%  
- **Test Accuracy:** ~XX%  

**Confusion Matrix Example:**  
![Confusion Matrix](results/confusion_matrix.png)  

**Training vs Validation Accuracy:**  
![Accuracy Graph](results/accuracy_graph.png)  

**Training vs Validation Loss:**  
![Loss Graph](results/loss_graph.png)  

---

## ✅ Conclusion  
This project provided hands-on experience with:  
- Handling large-scale histopathology datasets  
- Applying **data augmentation** to improve robustness  
- Comparing multiple **CNN architectures** and transfer learning strategies  
- Using **training optimization techniques** (EarlyStopping, LR scheduling)  
- Evaluating models using both **metrics and visualizations**  

The final models showed promising performance in distinguishing between **cancerous** and **non-cancerous** samples, demonstrating the potential of deep learning in medical image analysis.  

---

## 📌 Next Steps  
- Experiment with **more advanced EfficientNet variations (B4-B7)**  
- Apply **hyperparameter tuning** with Keras Tuner or Optuna  
- Deploy the best model as a **web application** for inference  

---

## 🖼️ Final Results and Visualizations  

📌 Add your results here by replacing placeholders with actual images/graphs.  

```markdown
![Confusion Matrix](results/confusion_matrix.png)  
![Accuracy Graph](results/accuracy_graph.png)  
![Loss Graph](results/loss_graph.png)  
