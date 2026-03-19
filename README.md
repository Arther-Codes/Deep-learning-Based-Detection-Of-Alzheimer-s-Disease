# 🧠 Deep Learning-Based Detection of Alzheimer’s Disease

## 📖 Project Overview
Alzheimer's Disease (AD) is a progressive neurodegenerative condition. This research provides a data-driven approach to detect AD early by analyzing structural brain changes in MRI scans. This work was presented at the **MLIP-2025 International Conference**.

## 🛠️ Model Architecture
Instead of using a basic CNN, I developed a custom pipeline which leverages **Transfer Learning** to handle the complexities of medical imaging:

* **Feature Extraction Base:** Utilized **Inception v3** to capture high-level hierarchical patterns from unprocessed neuroimaging data.
* **Global Average Pooling (GAP):** Added a GAP layer to reduce the dimensionality of the feature maps while maintaining critical spatial information and reducing the risk of overfitting.
* **Batch Normalization:** Implemented to standardize inputs between layers, which stabilized the training process and allowed for faster convergence.
* **Dense Layers & SoftMax:** The final classification is handled by fully connected layers and a SoftMax activation function to categorize scans into 3 stages: Normal, Mild, or Moderate Impairment.

## ⚙️ Optimization & Training
* **Optimizer:** Used the **Adam Optimizer**, which combines the benefits of Adaptive Gradient Algorithm (AdaGrad) and Root Mean Square Propagation (RMSProp) to minimize cross-entropy loss.
* **Preprocessing:** Applied **Min-Max Scaling** and **Standardization** to normalize pixel values, ensuring consistent input for the neural network.

## 📊 Research Results
The primary goal of this study was to accurately categorize MRI images into three stages: Normal, Mild Impairment, and Moderate Impairment.To provide a complete picture of the model's reliability, I implemented the following performance metrics used in the research:

* **Precision:** Measures the accuracy of positive predictions by dividing true positives (TP) by the total number of positive predictions.
    $$Precision = \frac{TP}{TP + FP}$$
* **Recall:** Determines the true positive rate, showing how effectively the model identifies actual disease biomarkers.
    $$Recall = \frac{TP}{TP + FN}$$
* **F1-Score:** The harmonic mean of precision and recall, used to balance the trade-offs between the two.
    $$F1\text{-}Score = 2 \times \frac{P \times R}{P + R}$$
* **Accuracy:** Evaluates the overall performance by comparing correct predictions against the total number of cases.
    $$Accuracy = \frac{TP + TN}{TP + FP + TN + FN}$$

| Metric | Healthy Brain | Moderate Impairment | Mild Impairment |
| :--- | :--- | :--- | :--- |
| **Precision** | **0.84** | 0.80 | 0.54 |
| **Recall** | 0.47 | 0.33 | 0.36 |
| **F1-Score** | **0.88** | 0.47 | 0.43 |

The results indicate that the combination of **Inception v3 transfer learning** and **fine-tuning** significantly enhances the model's ability to predict AD from MRI images compared to conventional methods[cite: 132, 133].
