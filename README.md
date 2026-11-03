# Comparative Study of Optimizers and Regularization Techniques

A comparative deep learning project that investigates how different optimizers, learning-rate schedules, and regularization techniques affect the performance of a fixed Convolutional Neural Network (CNN) using the Fashion-MNIST dataset.

## 📌 Project Overview

The performance of a CNN depends not only on its architecture but also on the training strategies used.

This project keeps the CNN architecture fixed and performs **15 controlled experiments** to compare different optimization algorithms and regularization techniques.

The main goal is to identify which configurations achieve better validation and test performance while analyzing their effects on model generalization.

## 🎯 Objectives

- Implement a fixed CNN architecture for image classification.
- Compare SGD, SGD with Momentum, RMSprop, and Adam optimizers.
- Evaluate Step Decay and Cosine Annealing learning-rate schedules.
- Study L2 Regularization, Dropout, Early Stopping, and Batch Normalization.
- Evaluate combinations of regularization techniques.
- Analyze training and validation accuracy and loss.
- Identify the best-performing configurations using validation and test results.

## 📊 Dataset

**Fashion-MNIST**

- Total images: 70,000
- Image dimensions: 28 × 28 pixels
- Image format: Grayscale
- Number of classes: 10

### Dataset Split

| Dataset | Number of Images |
|---|---:|
| Training | 48,000 |
| Validation | 12,000 |
| Testing | 10,000 |
| **Total** | **70,000** |

The official test set was kept separate from training and validation.

### Fashion-MNIST Classes

1. T-shirt/top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle boot

## 🧠 CNN Architecture

A single CNN architecture was maintained across all experiments to ensure a controlled comparison.

| Layer | Configuration |
|---|---|
| Input | 28 × 28 × 1 |
| Conv2D | 32 filters, 3 × 3, ReLU |
| Max Pooling | 2 × 2 |
| Conv2D | 64 filters, 3 × 3, ReLU |
| Max Pooling | 2 × 2 |
| Flatten | Feature conversion |
| Dense | 128 neurons, ReLU |
| Output | 10 neurons, Softmax |

**Baseline trainable parameters:** 421,642

Optional techniques such as L2 Regularization, Dropout, and Batch Normalization were applied during selected experiments.

## ⚙️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook / Google Colab

## 🔬 Experimental Setup

Common settings used across the experiments:

| Parameter | Value |
|---|---|
| Dataset | Fashion-MNIST |
| Batch Size | 64 |
| Maximum Epochs | 20 |
| Loss Function | Sparse Categorical Cross-Entropy |
| Random Seed | 42 |
| Initial Learning Rate | Experiment-dependent |
| Dropout Rate | 0.5 |
| L2 Strength | 0.0001 |
| Early Stopping Patience | 4 |

### 1. Optimizer Comparison

- Stochastic Gradient Descent (SGD)
- SGD with Momentum
- RMSprop
- Adam

### 2. Learning-Rate Schedules

- Step Decay
- Cosine Annealing

### 3. Individual Regularization Techniques

- L2 Regularization
- Dropout
- Early Stopping
- Batch Normalization

### 4. Combined Techniques

- L2 + Dropout
- L2 + Batch Normalization
- Dropout + Batch Normalization
- L2 + Dropout + Batch Normalization

**Total experiments: 15**

## 📈 Experimental Results

### Best Validation Accuracy

| Configuration | Validation Accuracy |
|---|---:|
| L2 + Dropout + Batch Normalization | **93.33%** |

### Best Test Accuracy

| Configuration | Test Accuracy |
|---|---:|
| Dropout + Batch Normalization | **92.79%** |

### Baseline vs Best Test Result

| Model | Test Accuracy |
|---|---:|
| Baseline SGD | 88.60% |
| Dropout + Batch Normalization | **92.79%** |

**Improvement: 4.19 percentage points over the baseline.**

### Key Observations

- Adam achieved 91.63% validation accuracy in the optimizer comparison.
- Adam with Cosine Annealing achieved 92.34% validation accuracy.
- L2 + Dropout + Batch Normalization achieved the highest validation accuracy of 93.33%.
- Dropout + Batch Normalization achieved the highest test accuracy of 92.79%.
- The best validation and test configurations were different.
- All 15 experiments were classified as reasonably fitted by the implemented notebook thresholds.

## 📉 Performance Analysis

The experiments were evaluated using:

- Training accuracy
- Validation accuracy
- Training loss
- Validation loss
- Test accuracy
- Test loss
- Training time
- Train-validation accuracy gap

Training and validation curves were generated to study model behavior and identify possible underfitting and overfitting.

## 🚀 How to Run the Project

1. Clone this repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   ```

2. Navigate to the project folder:

   ```bash
   cd YOUR-REPOSITORY
   ```

3. Install the required libraries:

   ```bash
   pip install tensorflow numpy pandas matplotlib jupyter
   ```

4. Open the Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open the project notebook and run the cells in order.

   You can also upload the notebook to Google Colab and execute it there.

## 📁 Project Structure

```text
Comparative-Study-Optimizers-Regularization/
│
├── README.md
├── Untitled2.ipynb
├── results/
│   ├── validation_results.csv
│   └── test_results.csv
│
├── graphs/
│   ├── test_accuracy.png
│   ├── validation_accuracy.png
│   ├── train_val_gap.png
│   └── training_time.png
│
└── presentation/
    └── Comparative_Study_Project_Presentation_FINAL.pptx
```

*Note: Update the filenames and folder structure to match the files actually uploaded to your repository.*

## 🔮 Future Scope

- Experiment with multiple random seeds.
- Perform extensive hyperparameter tuning.
- Evaluate the model using CIFAR-10 and other datasets.
- Generate confusion matrices.
- Analyze class-wise precision, recall, and F1-score.
- Explore additional CNN architectures and optimization techniques.

## 🏁 Conclusion

This project demonstrates that optimization and regularization strategies can significantly influence CNN performance, even when the architecture remains unchanged.

The best observed validation accuracy was **93.33%**, achieved using L2 + Dropout + Batch Normalization, while the best held-out test accuracy was **92.79%**, achieved using Dropout + Batch Normalization.

The results highlight the importance of evaluating both validation and test performance when selecting a deep learning configuration.

## 👩‍💻 Project Information

**Project Title:** Comparative Study of Optimizers and Regularization Techniques  
**Domain:** Artificial Intelligence & Deep Learning  
**Dataset:** Fashion-MNIST  
**Model:** Convolutional Neural Network (CNN)  
**Experiments:** 15

---

⭐ If you find this project useful, consider giving the repository a star!

