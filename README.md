# Optimization Dynamics Study in CNNs  
## An Empirical Investigation of Optimizer Behavior on CIFAR-10  

---

## 📌 Overview

This project investigates how optimization strategy influences convergence behavior, stability, and generalization performance in Convolutional Neural Networks (CNNs).

Instead of modifying architecture repeatedly, I fixed the model architecture and varied only optimization dynamics (learning rate, momentum, adaptive updates, and weight decay).

The objective was to isolate the impact of optimization configuration on training stability and test performance.

---

## 🎯 Research Objectives

- How sensitive is SGD to learning rate?
- Does momentum improve convergence stability?
- How do adaptive optimizers (Adam) compare to non-adaptive methods?
- Does decoupled weight decay (AdamW) improve generalization?
- How does optimizer choice influence the generalization gap?

---

## 📊 Dataset

- CIFAR-10 (60,000 RGB images, 10 classes)
- 50,000 training samples
- 10,000 test samples
- Images normalized to [0,1]
- One-hot encoded labels

---

## 🏗 Controlled Architecture

Architecture was kept constant across experiments:

- Two convolutional blocks (32 → 64 filters)
- Batch Normalization
- Max Pooling
- Dropout Regularization
- Fully Connected Layer (512 units)
- Softmax Output Layer
- L2 Weight Decay

This ensured performance differences arose solely from optimization dynamics.

---

## 🧪 Optimization Experiments

I evaluated:

- SGD (learning rate = 0.01)
- SGD + Momentum (0.9)
- Adam
- AdamW (decoupled weight decay)

All experiments used:
- Identical architecture
- Same batch size
- Same validation split
- Early stopping

---

## 📊 Final Results

| Optimizer        | Test Accuracy | Generalization Gap |
|------------------|--------------|--------------------|
| **AdamW**        | **76.21%**   | 0.0403             |
| SGD + Momentum   | 75.77%       | 0.0355             |
| Adam             | 74.70%       | 0.0325             |
| SGD (0.01)       | 74.41%       | 0.0054             |

---

## 📈 Key Observations

- SGD is sensitive to learning rate selection.
- Momentum improves convergence stability.
- Adam converges quickly but does not guarantee superior generalization.
- AdamW achieved the highest test accuracy through decoupled weight decay.
- Optimization configuration significantly influences final model performance.

---

## 🧠 Conclusion

Deep learning performance depends not only on model architecture but heavily on optimization strategy.

Careful tuning of:
- Learning rate
- Momentum
- Weight decay
- Early stopping

can meaningfully influence convergence behavior and generalization performance.

This study highlights the importance of disciplined experimentation when training deep neural networks.

---

## 🛠 Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn

---

## 🚀 How to Run

1. Clone the repository  
2. Install dependencies  
3. Run `CNN_Optimization_Study.ipynb`

---