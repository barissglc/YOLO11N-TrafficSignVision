# Traffic Signs Detection using YOLO11N

This repository contains output files, training process details, results, and sample prediction images for a model trained using the **YOLO11N** architecture to detect traffic signs.

## Contents

- [Project Summary](#project-summary)
- [Training Process](#training-process)
- [Results and Analysis](#results-and-analysis)

---

## Project Summary

This project presents a model trained with the **YOLO11N** architecture to detect traffic signs. The training process includes log files, graphs, and weight files, allowing for a detailed analysis of model performance. The model weight file used is `yolo11n.pt`.

---

## Training Process

- **Model:** YOLO11N  
- **Parameters:** The hyperparameters used during training are specified in the `args.yaml` file.  
- **Logs:** Detailed training logs (`events.out.tfevents.*`) can be analyzed using tools like TensorBoard.  
- **Weights:** The final trained model weights are stored in the `weights/` directory.

---

## Results and Analysis

The results obtained during training are supported by detailed visualizations to evaluate model performance and identify areas for improvement. Below are some of these visualizations along with brief explanations:

### 1. Confusion Matrix
![Confusion Matrix](/runs/detect/train/confusion_matrix.png)  
*This graphic illustrates misclassifications and highlights where the model struggles in distinguishing between classes.*

### 2. Normalized Confusion Matrix
![Normalized Confusion Matrix](/runs/detect/train/confusion_matrix_normalized.png)  
*A normalized version of the confusion matrix, providing a clearer view of class distribution percentages and misclassification rates.*

### 3. F1 Score Curve
![F1 Curve](/runs/detect/train/F1_curve.png)  
*Shows how the F1 score changes across different thresholds, helping to evaluate the balance between precision and recall.*

### 4. Precision-Recall Curve
![PR Curve](/runs/detect/train/PR_curve.png)  
*A visualization of precision and recall values, useful for assessing false positives and false negatives.*

### 5. Precision and Recall Curves
- **Precision Curve:**  
  ![Precision Curve](/runs/detect/train/P_curve.png)  
- **Recall Curve:**  
  ![Recall Curve](/runs/detect/train/R_curve.png)  
*These graphs separately illustrate the model’s precision and recall performance.*

### 6. Overall Performance Results
![Performance Results](/runs/detect/train/results.png)  
*Summarizes key metrics from training and validation processes, visually representing the numerical data from the `results.csv` file.*

### 7. Label Distribution and Correlogram
- **Label Distribution:**  
  ![Labels Distribution](/runs/detect/train/labels.jpg)  
- **Labels Correlogram:**  
  ![Labels Correlogram](/runs/detect/train/labels_correlogram.jpg)  
*Illustrates the distribution of traffic sign classes in the dataset and their correlation, providing insights into data balance and model focus areas.*

### 8. Validation Results
![Validation Prediction Example](/runs/detect/val/val_batch2_pred.jpg)  
*A sample image showcasing the model's predictions on validation data.*
